# Desabilitar Sleep, Hibernate, Suspend no Debian Linux

Como você pode desabilitar o estado suspenso sem precisar fazer login na sua interface gráfica de usuário.

Você já instalou o Deban e descobriu que toda vez que você deixa sua sessão ociosa por alguns minutos, o sistema entra em modo de suspensão?

Veja como você pode desabilitar o estado suspenso sem precisar fazer login na sua interface gráfica de usuário.

A seguir, descrevemos como você pode desabilitar o estado suspenso sem precisar fazer login na sua interface gráfica de usuário.

## Desabilitar Suspender via Terminal

Faça o seguinte comando para desabilitar o estado de suspensão no Debian Linux:

```
sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
```

## Verifique o status de suspensão via terminal

Faça o seguinte comando para verificar o status dos modos de estado de suspensão no Debian Linux:

```
sudo systemctl status sleep.target suspend.target hibernate.target hybrid-sleep.target
```

Um sistema com estado de suspensão desabilitado deve mostrar o seguinte:
```
○ sleep.target
     Loaded: masked (Reason: Unit sleep.target is masked.)
     Active: inactive (dead)

Mar 17 11:28:58 nosreme systemd[1]: Reached target sleep.target - Sleep.
Mar 17 11:30:13 nosreme systemd[1]: Stopped target sleep.target - Sleep.
Mar 17 11:50:13 nosreme systemd[1]: Reached target sleep.target - Sleep.
Mar 17 11:55:06 nosreme systemd[1]: Stopped target sleep.target - Sleep.

○ suspend.target
     Loaded: masked (Reason: Unit suspend.target is masked.)
     Active: inactive (dead)

Mar 17 11:30:13 nosreme systemd[1]: Reached target suspend.target - Suspend.
Mar 17 11:30:13 nosreme systemd[1]: Stopped target suspend.target - Suspend.
Mar 17 11:55:06 nosreme systemd[1]: Reached target suspend.target - Suspend.
Mar 17 11:55:06 nosreme systemd[1]: Stopped target suspend.target - Suspend.

○ hibernate.target
     Loaded: masked (Reason: Unit hibernate.target is masked.)
     Active: inactive (dead)

○ hybrid-sleep.target
     Loaded: masked (Reason: Unit hybrid-sleep.target is masked.)
     Active: inactive (dead)
```

Você pode ou não encontrar um registro smaller/larger/non-existing de suspensões do sistema. Observe isso de acordo com o seu sistema.

## Habilitar Suspender via Terminal

Faça o seguinte comando para reativar o estado de suspensão no Debian Linux:

```
sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target
```



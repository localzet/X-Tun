<p align="center"><a href="https://www.localzet.com" target="_blank">
  <img src="https://static.zorin.space/media/logos/LocalzetGroup.png" width="400">
</a></p>

# X-TUN - Tun2Socks

> Служба туннелирования для [X-WIN](https://github.com/localzet/x-win) (использует tun2socks и wintun)

X-TUN — это сервис, который позволяет туннелировать весь трафик системы. Он использует [tun2socks](https://github.com/xjasonlyu/tun2socks) и [wintun](https://www.wintun.net).<br/>
Эта служба автоматически создает сетевой интерфейс и устанавливает маршруты.

## Взаимодействие

После запуска службы на определенном порту вам необходимо подключиться к службе через сокет. Затем вы сможете использовать команды для управления службой. В настоящее время у нас есть две допустимые команды:

- `enable`: Включает службу туннелирования и настраивает сетевой интерфейс.
    ```
    -command=enable -device={device} -proxy={ip}:{port} -address={address} -server={server} -dns={dns}
    ```
- `disable`: Отключает службу туннелирования и удаляет сетевой интерфейс.
    ```
    -command=disable
    ```

## Требования

- Go https://go.dev/dl/
- .Net https://dotnet.microsoft.com/download

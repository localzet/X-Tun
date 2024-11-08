<p align="center"><a href="https://www.localzet.com" target="_blank">
  <img src="https://static.zorin.space/media/logos/ZorinProjectsSP.svg">
</a></p>

<p align="center">
  <a href="https://github.com/localzet/x-win/releases">
  <img src="https://img.shields.io/github/downloads/localzet/x-win/total.svg?label=%D0%A1%D0%BA%D0%B0%D1%87%D0%B8%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F" alt="Скачивания">
</a>
  <a href="https://github.com/localzet/x-win">
  <img src="https://img.shields.io/github/commit-activity/t/localzet/x-win?label=%D0%9A%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B" alt="Коммиты">
</a>
  <a href="https://github.com/localzet/x-win/releases/latest">
  <img src="https://img.shields.io/github/v/release/localzet/x-win?label=%D0%92%D0%B5%D1%80%D1%81%D0%B8%D1%8F" alt="Версия">
</a>
  <a href="https://github.com/localzet/x-win">
  <img src="https://img.shields.io/github/license/localzet/x-win?label=%D0%9B%D0%B8%D1%86%D0%B5%D0%BD%D0%B7%D0%B8%D1%8F" alt="Лицензия">
</a>
</p>

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

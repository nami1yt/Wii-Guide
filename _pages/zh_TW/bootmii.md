---
title: "進行 BootMii 備份"
---

{% include toc title="條目內容" %}

如果您需要有關本手冊的任何幫助，請加入 [RiiConnect24 的 Discord 伺服器](https://discord.gg/rc24)（推薦）或 [發送電子郵件至 support@riiiconnect24.net](mailto:support@riiiconnect24.net)。
{: .notice--info}

![BootMii Logo](/images/bootmii.png)

您需要一張 **SD 卡** 才能使用 BootMii 建立 NAND 備份。 如果您沒有任何可用的 SD 卡，您可以跳過此頁面，但強烈建議您盡快進行 NAND 備份。
{: .notice--warning}

建議使用 BootMii 作為 boot2，但只能安裝在早期的 Wii 主機中。 否則只能作為 IOS 安裝。
{: .notice--info}

BootMii 最重要的功能之一是能夠備份和恢復 Wii 的 NAND 儲存空間。 我們將討論如何執行 NAND 備份。 後續您將可以透過它進行系統還原。 定期或在對您的主機進行具風險的操作之前進行 NAND 備份是個好習慣（如果您知道自己在做什麼，您也不會進行任何有風險的操作）。

#### 前置需求

- 至少有 512MB 可用空間的 SD 卡

#### 操作說明

如果您的 BootMii 安裝於 boot2 當中，則需要通過重新啟動主機來啟動 BootMii。 如果是這種情況，請跳過步驟1和2。
{: .notice--info}

1. Launch the Homebrew Channel.
1. Press the HOME Button, then select "Launch BootMii". ![BootMii_Main](/images/BootMii/BootMii_Main.png)

如果 ` Launch BootMii ` 按鈕沒有出現的話，請 [重新啟動 HackMii Installer](hackmii)並安裝 BootMii。
{: .notice--info}

您將無法使用 Wii 控制器來控制 BootMii。 您必須使用主機上的 POWER 和 RESET 按鈕，或者將 GameCube 控制器插入端口 1 來控制 BootMii。 要在選項之間移動，請按 Wii 的 POWER 按鈕 (或 GameCube 控制器的左右十字鍵)。 要選擇選項，請按 Wii 的 RESET 按鈕 (或 GameCube 控制器的 A 鍵)。
{: .notice--info}

如果螢幕保持黑屏且光碟機的指示燈閃爍，那代表您的 SD 卡中缺少 BootMii 所需的檔案。 下載[此壓縮檔](https://static.hackmii.com/bootmii_sd_files.zip)並將其解壓縮到 SD 卡的根目錄，然後重試。
{: .notice--warning}

1. 選擇『Options』按鈕（帶齒輪的圖示）。 ![BootMii_Gears_Icon](/images/BootMii/BootMii_Gears_Icon.png)
1. 選擇『BackupMii』按鈕。 ![BootMii_Green_Arrow](/images/BootMii/BootMii_Green_Arrow.png)
   - NAND 備份將開始。 您將在螢幕上看到進度。
   - 若螢幕上出現『Bad Blocks』是正常的。 看到時不用特別擔心。
   - 在此步驟之後，BootMii 將驗證此備份。 Ideally, all the blocks should be green after the verification process.

1. 當備份完成後，按任意鍵退出 NAND 備份。 ![BootMii_NAND_Backup](/images/BootMii/BootMii_NAND_Backup.png)
1. 若要退出 BootMii，請按返回按鈕（帶箭頭的那個），然後您可以按 Wii 選單按鈕或 Homebrew 頻道按鈕退出您想要的地方。 ![BootMii_Return_Arrow](/images/BootMii/BootMii_Return_Arrow.png)

<div id="restore-notice" class="notice" markdown="1">
To restore from a NAND backup on your SD card, you can follow the instructions for [RestoreMii](bootmiirecover).
Please be reminded that <strong>restoring a NAND backup is usually a last resort,</strong> and that there often better ways to fix your brick.
Try your best to [identify your brick condition](bricks) and reverse the action that caused it in the first place.
</div>

To make sure you don’t lose the files, it's recommended to copy `nand.bin` and `keys.bin` from the root of your SD card to your computer.
{: .notice--info}

[Continue to Priiloader Installation](priiloader)<br> Priiloader adds a level of brick protection, and is highly recommended, especially if you were only able to install BootMii as IOS.
{: .notice--info}

---
description: La catégorie matérielle du système informatique regroupe des classes qui représentent des objets liés au matériel. Les exemples incluent les périphériques d’entrée, les disques durs, les cartes d’extension, les périphériques vidéo, les périphériques réseau et l’alimentation du système.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Classes matérielles du système informatique
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950646"
---
# <a name="computer-system-hardware-classes"></a>Classes matérielles du système informatique

La catégorie matérielle du système informatique regroupe des classes qui représentent des objets liés au matériel. Les exemples incluent les périphériques d’entrée, les disques durs, les cartes d’extension, les périphériques vidéo, les périphériques réseau et l’alimentation du système.

-   [Classes d’appareils de refroidissement](#cooling-device-classes)
-   [Classes d’appareils d’entrée](#input-device-classes)
-   [Classes de stockage de masse](#mass-storage-classes)
-   [Classes de carte mère, de contrôleur et de port](#motherboard-controller-and-port-classes)
-   [Classes de périphériques réseau](#networking-device-classes)
-   [Classes d’alimentation](#power-classes)
-   [Classes d’impression](#printing-classes)
-   [Classes de téléphonie](#telephony-classes)
-   [Classes vidéo et moniteur](#video-and-monitor-classes)
-   [Rubriques connexes](#related-topics)

## <a name="cooling-device-classes"></a>Classes d’appareils de refroidissement

La sous-catégorie appareils de refroidissement regroupe des classes qui représentent des ventilateurs instrumentables, des sondes de température et des appareils de réfrigération.



| Classe                                                     | Description                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**\_Ventilateur Win32**](win32-fan.md)                           | Représente les propriétés d’un appareil de ventilateur dans le système informatique.           |
| [**\_Heatpipe Win32**](win32-heatpipe.md)                 | Représente les propriétés d’un appareil de refroidissement de caloduc.                    |
| [**\_Réfrigération Win32**](win32-refrigeration.md)       | Représente les propriétés d’un appareil de réfrigération.                        |
| [**\_TemperatureProbe Win32**](win32-temperatureprobe.md) | Représente les propriétés d’un capteur de température (thermomètre électronique). |



 

## <a name="input-device-classes"></a>Classes d’appareils d’entrée

La sous-catégorie périphériques d’entrée regroupe des classes qui représentent des claviers et des dispositifs de pointage.



| Classe                                                 | Description                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**\_Clavier Win32**](win32-keyboard.md)             | Représente un clavier installé sur un système informatique exécutant Windows.                                               |
| [**\_PointingDevice Win32**](win32-pointingdevice.md) | Représente un périphérique d’entrée utilisé pour pointer vers et sélectionner des régions sur l’affichage d’un système informatique exécutant Windows. |



 

## <a name="mass-storage-classes"></a>Classes de stockage de masse

Les classes de la sous-catégorie stockage de masse représentent les périphériques de stockage tels que les lecteurs de disque dur, les lecteurs de CD-ROM et les lecteurs de bande.



| Classe                                                     | Description                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_AutochkSetting Win32**](win32-autochksetting.md)     | Représente les paramètres de l’opération de vérification de la validation d’un disque.                               |
| [**\_CDROMDrive Win32**](win32-cdromdrive.md)             | Représente un lecteur de CD-ROM sur un système informatique exécutant Windows.                              |
| [**\_DiskDrive Win32**](win32-diskdrive.md)               | Représente un lecteur de disque physique tel qu’il est vu par un ordinateur exécutant le système d’exploitation Windows. |
| [**\_FloppyDrive Win32**](win32-floppydrive.md)           | Gère les fonctionnalités d’un lecteur de disquette.                                             |
| [**\_PhysicalMedia Win32**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Représente tout type de documentation ou de support de stockage.                                      |
| [**Win32 \_ de Win32**](win32-tapedrive.md)               | Représente un lecteur de bande sur un système informatique exécutant Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Classes de carte mère, de contrôleur et de port

La carte mère, les contrôleurs et les groupes de sous-catégories regroupent les classes qui représentent les périphériques système. Les exemples incluent la mémoire système, la mémoire cache et les contrôleurs.



| Classe                                                                       | Description                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_1394Controller Win32**](win32-1394controller.md)                       | Représente les fonctionnalités et la gestion d’un contrôleur 1394.<br/>                                                                                                                                               |
| [**\_1394ControllerDevice Win32**](win32-1394controllerdevice.md)           | Met en relation le contrôleur de bus série haute vitesse (IEEE 1394 FireWire) et l’instance du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui lui est connectée.<br/>                                                            |
| [**\_AllocatedResource Win32**](win32-allocatedresource.md)                 | Établit une relation entre un périphérique logique et une ressource système.<br/>                                                                                                                                                                 |
| [**\_AssociatedProcessorMemory Win32**](win32-associatedprocessormemory.md) | Établit une relation entre un processeur et sa mémoire cache.<br/>                                                                                                                                                                      |
| [**\_Carte mère Win32**](win32-baseboard.md)                                 | Représente une carte mère (également appelée carte mère ou carte système).<br/>                                                                                                                                          |
| [**\_BIOS Win32**](win32-bios.md)                                           | Représente les attributs des services d’entrée ou de sortie de base du système de l’ordinateur qui sont installés sur l’ordinateur.<br/>                                                                                   |
| [**\_Bus Win32**](win32-bus.md)                                             | Représente un bus physique tel qu’il est vu par un système d’exploitation Windows.<br/>                                                                                                                                               |
| [**\_CacheMemory Win32**](win32-cachememory.md)                             | Représente la mémoire cache (interne et externe) sur un système informatique.<br/>                                                                                                                                          |
| [**\_ControllerHasHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Représente les hubs en aval du contrôleur USB (Universal Serial Bus).<br/>                                                                                                                                 |
| [**\_DeviceBus Win32**](win32-devicebus.md)                                 | Établit une relation entre un bus système et un périphérique logique à l’aide du bus.<br/>                                                                                                                                                       |
| [**\_DeviceMemoryAddress Win32**](win32-devicememoryaddress.md)             | Représente une adresse mémoire de l’appareil sur un système Windows.<br/>                                                                                                                                                        |
| [**\_DeviceSettings Win32**](win32-devicesettings.md)                       | Établit une relation entre un périphérique logique et un paramètre qui lui est appliqué.<br/>                                                                                                                                              |
| [**\_Canal DMA Win32**](win32-dmachannel.md)                               | Représente un canal d’accès direct à la mémoire (DMA) sur un système informatique exécutant Windows.<br/>                                                                                                                          |
| [**\_FloppyController Win32**](win32-floppycontroller.md)                   | Représente les capacités et la capacité de gestion d’un contrôleur de lecteur de disquette.<br/>                                                                                                                         |
| [**\_IDEController Win32**](win32-idecontroller.md)                         | Représente les fonctionnalités d’un appareil de contrôleur IDE (Integrated Drive Electronics).<br/>                                                                                                                        |
| [**\_IDEControllerDevice Win32**](win32-idecontrollerdevice.md)             | Classe d’association qui associe un contrôleur IDE et l’appareil logique.<br/>                                                                                                                                       |
| [**\_InfraredDevice Win32**](win32-infrareddevice.md)                       | Représente les fonctionnalités et la gestion d’un périphérique infrarouge.<br/>                                                                                                                                              |
| [**\_IRQResource Win32**](win32-irqresource.md)                             | Représente un numéro d’interruption (IRQ) sur un système informatique Windows.<br/>                                                                                                                                |
| [**\_MemoryArray Win32**](win32-memoryarray.md)                             | Représente les propriétés du tableau de la mémoire système de l’ordinateur et des adresses mappées.<br/>                                                                                                                            |
| [**\_MemoryArrayLocation Win32**](win32-memoryarraylocation.md)             | Établit un lien entre un tableau de mémoire logique et le tableau de mémoire physique sur lequel il se trouve.<br/>                                                                                                                             |
| [**\_MemoryDevice Win32**](win32-memorydevice.md)                           | Représente les propriétés du périphérique de mémoire d’un système d’ordinateur, ainsi que les adresses mappées qui lui sont associées.<br/>                                                                                                     |
| [**\_MemoryDeviceArray Win32**](win32-memorydevicearray.md)                 | Met en relation un périphérique de mémoire et le tableau de mémoire dans lequel il réside.<br/>                                                                                                                                              |
| [**\_MemoryDeviceLocation Win32**](win32-memorydevicelocation.md)           | Classe d’association qui associe un périphérique mémoire et la mémoire physique sur laquelle il existe.<br/>                                                                                                                     |
| [**\_MotherboardDevice Win32**](win32-motherboarddevice.md)                 | Représente un appareil qui contient les composants centraux du système informatique exécutant Windows.<br/>                                                                                                               |
| [**\_OnBoardDevice Win32**](win32-onboarddevice.md)                         | Représente les périphériques d’adaptateur courants intégrés à la carte mère (carte système).<br/>                                                                                                                                   |
| [**\_ParallelPort Win32**](win32-parallelport.md)                           | Représente les propriétés d’un port parallèle sur un système d’ordinateur exécutant Windows.<br/>                                                                                                                             |
| [**\_PCMCIAController Win32**](win32-pcmciacontroller.md)                   | Gère les fonctionnalités d’un périphérique de contrôleur PCMCIA (Personal Computer Memory Card interface).<br/>                                                                                                      |
| [**\_PhysicalMemory Win32**](win32-physicalmemory.md)                       | Représente un périphérique de mémoire physique situé sur un ordinateur, tel qu’il est disponible pour le système d’exploitation.<br/>                                                                                                                |
| [**\_PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md)             | Représente des détails sur la mémoire physique du système de l’ordinateur.<br/>                                                                                                                                                |
| [**\_PhysicalMemoryLocation Win32**](win32-physicalmemorylocation.md)       | Établit une relation entre un tableau de la mémoire physique et sa mémoire physique.<br/>                                                                                                                                                   |
| [**\_PNPAllocatedResource Win32**](win32-pnpallocatedresource.md)           | Représente une association entre des unités logiques et des ressources système.<br/>                                                                                                                                        |
| [**\_PNPDevice Win32**](win32-pnpdevice.md)                                 | Met en relation un appareil (connu pour Configuration Manager en tant que PNPEntity) et la fonction qu’il exécute.<br/>                                                                                                                |
| [**\_PNPEntity Win32**](win32-pnpentity.md)                                 | Représente les propriétés d’un appareil Plug-and-Play.<br/>                                                                                                                                                           |
| [**\_PortConnector Win32**](win32-portconnector.md)                         | Représente les ports de connexion physique, tels que la broche mâle DB-25, Centronics et PS/2.<br/>                                                                                                                            |
| [**\_PortResource Win32**](win32-portresource.md)                           | Représente un port d’e/s sur un système informatique exécutant Windows.<br/>                                                                                                                                                   |
| [**\_Processeur Win32**](win32-processor.md)                                 | Représente un appareil qui permet d’interpréter une séquence d’instructions de machine sur un système informatique exécutant Windows.<br/>                                                                                           |
| [**\_SCSIController Win32**](win32-scsicontroller.md)                       | Représente un contrôleur SCSI (Small Computer System Interface) sur un système informatique exécutant Windows.<br/>                                                                                                           |
| [**\_SCSIControllerDevice Win32**](win32-scsicontrollerdevice.md)           | Établit une relation entre un contrôleur SCSI et l’unité logique (lecteur de disque) qui y est connecté.<br/>                                                                                                                                 |
| [**\_SerialPort Win32**](win32-serialport.md)                               | Représente un port série sur un système informatique exécutant Windows.<br/>                                                                                                                                                 |
| [**\_SerialPortConfiguration Win32**](win32-serialportconfiguration.md)     | Représente les paramètres de transmission de données sur un port série Windows.<br/>                                                                                                                                        |
| [**\_SerialPortSetting Win32**](win32-serialportsetting.md)                 | Établit une relation entre un port série et ses paramètres de configuration.<br/>                                                                                                                                                          |
| [**\_SMBIOSMemory Win32**](win32-smbiosmemory.md)                           | Représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.<br/>                                                                                                                                  |
| [**\_SoundDevice Win32**](win32-sounddevice.md)                             | Représente les propriétés d’un périphérique audio sur un système informatique exécutant Windows.<br/>                                                                                                                              |
| [**\_SystemBIOS Win32**](win32-systembios.md)                               | Met en relation un système informatique (y compris des données telles que les propriétés de démarrage, les fuseaux horaires, les configurations de démarrage ou les mots de passe d’administration) et un BIOS système (services, langues et propriétés de gestion du système).<br/> |
| [**\_SystemDriverPNPEntity Win32**](win32-systemdriverpnpentity.md)         | Met en relation un appareil Plug-and-Play sur le système informatique Windows et le pilote qui prend en charge le périphérique Plug-and-Play.<br/>                                                                                           |
| [**\_SystemEnclosure Win32**](win32-systemenclosure.md)                     | Représente les propriétés associées à un boîtier système physique.<br/>                                                                                                                                         |
| [**\_SystemMemoryResource Win32**](win32-systemmemoryresource.md)           | Représente une ressource de mémoire système sur un système Windows.<br/>                                                                                                                                                       |
| [**\_SystemSlot Win32**](win32-systemslot.md)                               | Représente les points de connexion physiques, y compris les ports, les emplacements de carte mère et les périphériques, ainsi que les points de connexion propriétaires.<br/>                                                                                  |
| [**\_USBController Win32**](win32-usbcontroller.md)                         | Gère les fonctionnalités d’un contrôleur USB (Universal Serial Bus).<br/>                                                                                                                                           |
| [**\_USBControllerDevice Win32**](win32-usbcontrollerdevice.md)             | Établit une relation entre un contrôleur USB et les instances du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui y sont connectés.<br/>                                                                                                    |
| [**\_USBHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Représente les caractéristiques de gestion d’un concentrateur USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Classes de périphériques réseau

La sous-catégorie appareils de mise en réseau regroupe des classes qui représentent le contrôleur d’interface réseau, ses configurations et ses paramètres.



| Classe                                                                           | Description                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NetworkAdapter Win32**](win32-networkadapter.md)                           | Représente une carte réseau sur un système informatique exécutant Windows.<br/>                                                                                                                                          |
| [**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) | Représente les attributs et les comportements d’une carte réseau. La prise en charge de la classe n’est pas garantie après la ratification de la spécification réseau CIM de la DMTF (Distributed Management Task Force).<br/> |
| [**\_NetworkAdapterSetting Win32**](win32-networkadaptersetting.md)             | Établit une relation entre une carte réseau et ses paramètres de configuration.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Classes d’alimentation

Les classes de sous-catégorie Power regroupent les classes qui représentent les alimentations, les batteries et les événements liés à ces appareils.



| Classe                                                             | Description                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_Batterie Win32**](win32-battery.md)                           | Représente une batterie connectée au système de l’ordinateur.<br/>                                     |
| [**\_CurrentProbe Win32**](win32-currentprobe.md)                 | Représente les propriétés d’un capteur d’analyse actuel (Ammeter).<br/>                        |
| [**\_PortableBattery Win32**](win32-portablebattery.md)           | Représente les propriétés d’une batterie portable, comme celle utilisée pour un ordinateur notebook.<br/> |
| [**\_PowerManagementEvent Win32**](win32-powermanagementevent.md) | Représente les événements de gestion de l’alimentation qui résultent des modifications de l’état d’alimentation.<br/>                     |
| [**\_VoltageProbe Win32**](win32-voltageprobe.md)                 | Représente les propriétés d’un capteur de tension (tensiomètre électronique).<br/>                      |



 

## <a name="printing-classes"></a>Classes d’impression

La sous-catégorie impression regroupe les classes qui représentent les imprimantes, les configurations d’imprimante et les travaux d’impression.



| Classe                                                             | Description                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DriverForDevice Win32**](win32-driverfordevice.md)           | Établit une relation entre une imprimante et un pilote d’imprimante.<br/>                                                                                        |
| [**\_Imprimante Win32**](win32-printer.md)                           | Représente un appareil connecté à un système d’ordinateur exécutant Windows qui est capable de reproduire une image visuelle sur un support.<br/> |
| [**\_PrinterConfiguration Win32**](win32-printerconfiguration.md) | Définit la configuration d’un périphérique d’impression.<br/>                                                                               |
| [**\_PrinterController Win32**](win32-printercontroller.md)       | Établit une relation entre une imprimante et l’appareil local auquel l’imprimante est connectée.<br/>                                                     |
| [**\_PrinterDriver Win32**](win32-printerdriver.md)               | Représente les pilotes pour une instance d' [**\_ imprimante Win32**](win32-printer.md) .<br/>                                                |
| [**\_PrinterDriverDll Win32**](win32-printerdriverdll.md)         | Établit une relation entre une imprimante locale et son fichier de pilote (et non le pilote lui-même).<br/>                                                          |
| [**\_PrinterSetting Win32**](win32-printersetting.md)             | Établit une relation entre une imprimante et ses paramètres de configuration.<br/>                                                                             |
| [**\_PrintJob Win32**](win32-printjob.md)                         | Représente un travail d’impression généré par une application Windows.<br/>                                                              |
| [**\_TCPIPPrinterPort Win32**](win32-tcpipprinterport.md)         | Représente un point d’accès au service TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Classes de téléphonie

La sous-catégorie téléphonie regroupe des classes qui représentent les périphériques de modem « Plain Old Telephone » et leurs connexions série associées.



| Classe                                                               | Description                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_POTSModem Win32**](win32-potsmodem.md)                         | Représente les services et les caractéristiques d’un modem POTS (Plain Old Telephone Service) sur un système informatique exécutant Windows.<br/> |
| [**\_POTSModemToSerialPort Win32**](win32-potsmodemtoserialport.md) | Établit une relation entre un modem et le port série utilisé par le modem.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Classes vidéo et moniteur

Les classes de sous-catégorie vidéo et moniteurs qui représentent des analyses, des cartes vidéo et leurs paramètres associés.



| Classe                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Desktopmonitor Win32**](win32-desktopmonitor.md)                                 | Représente le type de moniteur ou d’écran d’affichage attaché au système de l’ordinateur.<br/>                                                                                                                                                                                                                                                                                       |
| [**\_DisplayControllerConfiguration Win32**](win32-displaycontrollerconfiguration.md) | Représente les informations de configuration de la carte vidéo d’un système informatique exécutant Windows. Cette classe est obsolète. À la place de cette classe, utilisez les propriétés des classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ desktopmonitor**](win32-desktopmonitor.md)et [CIM \_ VideoControllerResolution](cim-videocontrollerresolution.md) .<br/> |
| [**\_VideoController Win32**](win32-videocontroller.md)                               | Représente les capacités et la capacité de gestion du contrôleur vidéo sur un système informatique exécutant Windows.<br/>                                                                                                                                                                                                                                                       |
| [**\_VideoSettings Win32**](win32-videosettings.md)                                   | Met en relation un contrôleur vidéo et des paramètres vidéo qui peuvent être appliqués à celui-ci.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 


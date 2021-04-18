---
title: Interfaces de PC virtuels Windows
description: Les interfaces suivantes sont prises en charge par Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- PC virtuels Windows Virtual PC, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512317"
---
# <a name="windows-virtual-pc-interfaces"></a>Interfaces de PC virtuels Windows

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Les interfaces suivantes sont prises en charge par Windows Virtual PC.



| Interface                                                                             | Description                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Permet d’accéder aux informations relatives à la comptabilité pour un ordinateur virtuel.<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Contrôle les paramètres d’affichage d’une machine virtuelle.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Contrôle un lecteur de CD-ROM ou de DVD-ROM au sein d’une machine virtuelle.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Définit la collection de lecteurs de CD et de DVD au sein de la machine virtuelle.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Définit l’interface d’événements sortants pour l’interface [**IVMDVDDrive**](ivmdvddrive.md) .<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Contrôle un lecteur de disquette au sein d’une machine virtuelle.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Définit une collection de lecteurs de disquettes au sein de la machine virtuelle.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Définit l’interface d’événements sortants pour l’interface [**IVMFloppyDrive**](ivmfloppydrive.md) .<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Définit le système d’exploitation invité en cours d’exécution au sein d’une machine virtuelle.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Permet d’accéder à une image de disque dur.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Définit la connexion d’un disque dur au sein de la machine virtuelle.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Définit la collection de connexions de disque dur au sein de la machine virtuelle.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Récupère des informations sur l’ordinateur hôte.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Contrôle le périphérique clavier au sein d’une machine virtuelle.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Contrôle le périphérique de la souris au sein d’une machine virtuelle.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Sert d’interface à une carte d’interface réseau virtuelle (NIC) au sein d’une machine virtuelle.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Définit une collection de cartes réseau virtuelles au sein d’une machine virtuelle.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Définit un port parallèle à l’intérieur d’une machine virtuelle.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Définit la collection de ports parallèles dans la machine virtuelle.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Définit un port série à l’intérieur d’une machine virtuelle.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Définit la collection de ports série au sein de la machine virtuelle.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Utilisé pour surveiller et contrôler les tâches asynchrones pour différentes méthodes.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Définit la collection d’objets Task au sein d’une machine virtuelle.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Définit l’interface pour un périphérique USB attaché au système hôte.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Définit la collection des périphériques USB attachés au système hôte.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Définit l’interface pour une machine virtuelle.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Définit la collection de machines virtuelles dans Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Définit l’interface d’événements sortants pour l’interface [**IVMVirtualMachine**](ivmvirtualmachine.md) .<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Définit un réseau virtuel.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Définit une collection d’objets [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Définit l’objet d’application de PC virtuel Windows de niveau supérieur.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Définit l’interface d’événements sortants pour l’interface [**IVMVirtualPC**](ivmvirtualpc.md) .<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Remarque pour les développeurs sur Windows 64 bits

Sur les éditions 64 bits de Windows, la bibliothèque de types pour Windows Virtual PC se trouve dans un fichier binaire 64 bits (VPC.exe) dans le répertoire% WinDir% \\ system32. Ce répertoire n’est pas visible par défaut aux processus 32 bits ; WOW64 mappe tous les accès au répertoire% WinDir% \\ system32 dans le répertoire% windir% \\ SysWOW64 par défaut. Visual Studio est un binaire 32 bits et ne peut donc pas ouvrir le fichier à cet emplacement. Pour générer un assembly d’interopérabilité pour Windows Virtual PC, utilisez TlbImp.exe, fourni avec Visual Studio et le SDK Windows. Pour générer *Microsoft.VirtualPC.Interop.dll*, utilisez la ligne de commande suivante :

**TlbImp.exe/out : * * * Microsoft.VirtualPC.Interop.dll* **/Namespace : Microsoft. VirtualPC. Interop% WinDir% \\ system32 \\VPC.exe**

D’autres solutions incluent la copie VPC.exe dans un répertoire différent où le compilateur peut le trouver, ou l’utilisation de l’outil OleView.exe à partir du SDK Windows pour extraire un fichier. idl de la bibliothèque de types dans VPC.exe.

 


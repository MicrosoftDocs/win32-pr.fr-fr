---
title: Interface IVMVirtualPC (VPCCOMInterfaces. h)
description: Définit l’objet d’application de PC virtuel Windows de niveau supérieur. Tous les autres objets de l’interface Windows Virtual PC sont récupérés via cet objet.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Virtual PC de l’interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d674fd1cbbe6c51881d15f91f0ebfb20f4f6749
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032985"
---
# <a name="ivmvirtualpc-interface"></a>Interface IVMVirtualPC

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’objet d’application de PC virtuel Windows de niveau supérieur. Tous les autres objets de l’interface Windows Virtual PC sont récupérés via cet objet.

**IVMVirtualPC** peut informer les clients sur les événements à l’aide de l’interface sortante [**IVMVirtualPCEvents**](ivmvirtualpcevents.md) .

## <a name="members"></a>Membres

L’interface **IVMVirtualPC** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPC** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMVirtualPC** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Crée un disque dur virtuel de différenciation.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Crée un disque dur virtuel de redimensionnement dynamique.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Crée un disque dur virtuel de taille fixe.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Crée un fichier image de disquette.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Crée une nouvelle configuration d’ordinateur virtuel et récupère l’objet ordinateur virtuel.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Supprime une configuration d’ordinateur virtuel.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Récupère un objet ordinateur virtuel qui correspond à la configuration demandée.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Récupère un objet réseau virtuel qui correspond au nom demandé.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Récupère la valeur du paramètre de configuration spécifié.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Récupère un tableau de fichiers de DVD connus.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Récupère un tableau de fichiers de disquettes virtuelles connus.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Récupère le type d’un fichier image de disquette existant.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Récupère un objet correspondant à un fichier image de disque existant.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Récupère un tableau de fichiers de disque dur virtuel connus.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Récupère un tableau de fichiers de configuration d’ordinateur virtuel connus.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Inscrit une configuration d’ordinateur virtuel existante et récupère l’objet ordinateur virtuel.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Supprime la valeur du paramètre de configuration spécifié.<br/>                                     |
| [**SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)                         | Définit la valeur du paramètre de configuration spécifié.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Annule l’inscription d’une configuration d’ordinateur virtuel sans supprimer le fichier de configuration.<br/>          |



 

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualPC** possède les propriétés suivantes.



| Propriété                                                                                   | Type d’accès           | Description                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Lecture/écriture<br/> | Répertoire par défaut dans lequel rechercher les fichiers de configuration d’ordinateur virtuel disponibles.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Lecture seule<br/>  | Informations sur l’ordinateur physique.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Lecture seule<br/>  | Nombre maximal de lecteurs de disquette par ordinateur virtuel.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Lecture seule<br/>  | Quantité maximale autorisée de mémoire physique par ordinateur virtuel, en mégaoctets.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Lecture seule<br/>  | Nombre maximal d’interfaces réseau par ordinateur virtuel.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Lecture seule<br/>  | Nombre maximal de bus autorisés pour l’IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Lecture seule<br/>  | Nombre maximal de ports parallèles par ordinateur virtuel.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Lecture seule<br/>  | Nombre maximal de ports série par ordinateur virtuel.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Lecture seule<br/>  | Quantité minimale autorisée de mémoire physique par ordinateur virtuel, en mégaoctets.<br/>                                                       |
| [**Nom**](ivmvirtualpc-name.md)<br/>                                               | Lecture seule<br/>  | Nom de l’application Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Lecture/écriture<br/> | Chemins d’accès du système de fichiers utilisés pour rechercher des fichiers associés à Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Lecture seule<br/>  | Quantité maximale autorisée de mémoire physique par ordinateur virtuel, en mégaoctets, pour éviter des conditions de mémoire insuffisante sur l’ordinateur hôte.<br/> |
| [**Tâches**](ivmvirtualpc-tasks.md)<br/>                                             | Lecture seule<br/>  | Collection de tâches.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Lecture seule<br/>  | Collection énumérable d’interfaces réseau non connectées.<br/>                                                                                |
| [**Activité**](ivmvirtualpc-uptime.md)<br/>                                           | Lecture seule<br/>  | Nombre de secondes d’exécution de l’application Windows Virtual PC.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Lecture seule<br/>  | Collection énumérable de tous les périphériques USB connectés à l’hôte.<br/>                                                                         |
| [**Version**](ivmvirtualpc-version.md)<br/>                                         | Lecture seule<br/>  | Version de cette instance de Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Lecture seule<br/>  | Collection énumérable de machines virtuelles.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Lecture seule<br/>  | Collection énumérable de réseaux virtuels.<br/>                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



 


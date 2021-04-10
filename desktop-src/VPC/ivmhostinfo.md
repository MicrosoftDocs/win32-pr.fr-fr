---
title: Interface IVMHostInfo (VPCCOMInterfaces. h)
description: Récupère des informations sur l’ordinateur hôte. Un objet IVMHostInfo est retourné à partir de la propriété HostInfo IVMVirtualPC.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- Virtual PC de l’interface IVMHostInfo
- IVMHostInfo interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ca5f296dd4a7437ea136dbaee0d04c68a93efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103593"
---
# <a name="ivmhostinfo-interface"></a>Interface IVMHostInfo

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère des informations sur l’ordinateur hôte. Un objet **IVMHostInfo** est retourné à partir de la propriété [**IVMVirtualPC :: hostInfo**](ivmvirtualpc-hostinfo.md) .

## <a name="members"></a>Membres

L’interface **IVMHostInfo** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHostInfo** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMHostInfo** possède les propriétés suivantes.



| Propriété                                                                                  | Type d’accès          | Description                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Lecture seule<br/> | Les lettres de lecteur associées aux périphériques CD et DVD hôte.<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | Lecture seule<br/> | Les lettres de lecteur associées aux lecteurs de disquettes de l’ordinateur hôte.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Lecture seule<br/> | Nombre de processeurs logiques dans l’ordinateur hôte.<br/>                                   |
| [**Mémoire**](ivmhostinfo-memory.md)<br/>                                           | Lecture seule<br/> | Quantité totale de mémoire physique de l’ordinateur hôte, en mégaoctets.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Lecture seule<br/> | Quantité de mémoire physique disponible sur l’ordinateur hôte, en mégaoctets.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Lecture seule<br/> | Quantité de mémoire physique disponible sur l’ordinateur hôte, en mégaoctets, sous la forme d’une chaîne.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Lecture seule<br/> | Quantité totale de mémoire physique de l’ordinateur hôte, en mégaoctets, sous la forme d’une chaîne.<br/>     |
| [**TECHNOLOGIE**](ivmhostinfo-mmx.md)<br/>                                                 | Lecture seule<br/> | Indique si le processeur prend en charge le jeu d’instructions MMX.<br/>                       |
| [**NetworkAdapters**](ivmhostinfo-networkadapters.md)<br/>                         | Lecture seule<br/> | Collection énumérable de cartes réseau dans l’ordinateur hôte.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Lecture seule<br/> | Collection énumérable d’adresses TCP/IP sur l’ordinateur hôte.<br/>                       |
| [**OperatingSystem**](ivmhostinfo-operatingsystem.md)<br/>                         | Lecture seule<br/> | Le système d’exploitation en cours d’exécution sur l’ordinateur hôte.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Lecture seule<br/> | Version principale du système d’exploitation en cours d’exécution sur l’ordinateur hôte.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Lecture seule<br/> | Version mineure du système d’exploitation en cours d’exécution sur l’ordinateur hôte.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Lecture seule<br/> | Les informations Service Pack du système d’exploitation en cours d’exécution sur l’ordinateur hôte.<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | Lecture seule<br/> | Version du système d’exploitation en cours d’exécution sur l’ordinateur hôte.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Lecture seule<br/> | Port parallèle hôte qui peut être attaché à l’invité.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Lecture seule<br/> | Nombre de processeurs physiques sur l’ordinateur hôte.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Lecture seule<br/> | Liste des fonctionnalités prises en charge par le processeur hôte.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Lecture seule<br/> | Fabricant du processeur hôte.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Lecture seule<br/> | Vitesse du processeur hôte, en mégahertz (MHz) ou gigahertz (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Lecture seule<br/> | Vitesse du processeur hôte, en mégahertz ou gigahertz, sous la forme d’une chaîne.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Lecture seule<br/> | Version du processeur hôte.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Lecture seule<br/> | Noms des ports série associés aux ports série de l’ordinateur hôte.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Lecture seule<br/> | Indique si le processeur prend en charge le jeu d’instructions SSE.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Lecture seule<br/> | Indique si le processeur prend en charge le jeu d’instructions SSE2.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Lecture seule<br/> | Indique si le processeur prend en charge le jeu d’instructions 3DNow.<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | Lecture seule<br/> | Heure UTC de l’ordinateur hôte.<br/>                                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc<br/>                |



 


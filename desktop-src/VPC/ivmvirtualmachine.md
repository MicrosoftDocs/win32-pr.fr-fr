---
title: Interface IVMVirtualMachine (VPCCOMInterfaces. h)
description: Définit l’interface pour un ordinateur virtuel.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- Virtual PC de l’interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2f50c5279bafd12d8edd01a47e9cbcb1a3cc3bb2b89ea140e46cf06c0aa06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124679"
---
# <a name="ivmvirtualmachine-interface"></a>Interface IVMVirtualMachine

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface pour un ordinateur virtuel. **IVMVirtualMachine** peut informer les clients des événements à l’aide de l’interface sortante [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) . Les objets **IVMVirtualMachine** sont retournés à partir de méthodes [**IVMVirtualPC**](ivmvirtualpc.md) telles que [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md), [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)et [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md). Vous pouvez également récupérer un objet **IVMVirtualMachine** à partir de l’objet [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md) retourné à partir de la propriété [**IVMVirtualPC :: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membres

L’interface **IVMVirtualMachine** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachine** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMVirtualMachine** possède ces méthodes.



| Méthode                                                                           | Description                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Ajoute un nouveau lecteur de CD ou de DVD à la machine virtuelle.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Ajoute une nouvelle connexion de disque dur à la machine virtuelle.<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Ajoute une interface réseau à la machine virtuelle.<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | Attache un périphérique USB à un ordinateur virtuel.<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | Libère un périphérique USB d’un ordinateur virtuel.<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | Ignore toutes les informations d’état enregistrées pour un ordinateur virtuel enregistré.<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | Ignore les disques d’annulations virtuelles.<br/>                                                                |
| [**GetActivationValue**](ivmvirtualmachine-getactivationvalue.md)               | Récupère la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Récupère la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | Fusionne les disques d’annulations virtuelles.<br/>                                                                  |
| [**Suspendre**](ivmvirtualmachine-pause.md)                                         | Suspend la machine virtuelle.<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | Supprime la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Supprime la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.<br/>              |
| [**RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Supprime le lecteur de CD ou de DVD spécifié de la machine virtuelle.<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Supprime la connexion de disque dur spécifiée de l’ordinateur virtuel.<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | Supprime une interface réseau de la machine virtuelle.<br/>                                           |
| [**Initialisation**](ivmvirtualmachine-reset.md)                                         | Réinitialise l’ordinateur virtuel.<br/>                                                                     |
| [**Reprendre**](ivmvirtualmachine-resume.md)                                       | Reprend l’ordinateur virtuel.<br/>                                                                    |
| [**Enregistrer**](ivmvirtualmachine-save.md)                                           | Enregistre l’état de la machine virtuelle.<br/>                                                                |
| [**SetActivationValue**](ivmvirtualmachine-setactivationvalue.md)               | Définit la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.<br/>                    |
| [**SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)         | Définit la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | Configure un canal de communication entre l’hôte et l’invité.<br/>                                         |
| [**Démarrage**](ivmvirtualmachine-startup.md)                                     | Démarre l’ordinateur virtuel à partir de l’état non initialisé ou enregistré.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Démarre l’ordinateur virtuel à partir de l’état non initialisé ou enregistré, avec des options avancées.<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | Met l’ordinateur virtuel hors tension.<br/>                                                                  |



 

### <a name="properties"></a>Propriétés

L’interface **IVMVirtualMachine** possède les propriétés suivantes.



| Propriété                                                                            | Type d’accès           | Description                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comptabilité**](ivmvirtualmachine-accountant.md)<br/>                       | Lecture seule<br/>  | Un comptable pour cette machine virtuelle.<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Lecture seule<br/>  | Tableau qui indique le type de lecteur attaché à chaque emplacement de la machine virtuelle.<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Lecture/écriture<br/> | Numéro de série du tableau de base.<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | Lecture/écriture<br/> | GUID du BIOS.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Lecture/écriture<br/> | Numéro de série du BIOS.<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Lecture/écriture<br/> | Étiquette de la ressource du châssis.<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Lecture/écriture<br/> | Numéro de série du châssis.<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | Lecture seule<br/>  | Identificateur unique de la machine virtuelle.<br/>                                                                                      |
| [**Affichage**](ivmvirtualmachine-display.md)<br/>                             | Lecture seule<br/>  | Affichage vidéo de la machine virtuelle.<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Lecture seule<br/>  | Une collection énumérable de lecteurs de CD et de DVD attachés à la machine virtuelle.<br/>                                                      |
| [**Fichier**](ivmvirtualmachine-file.md)<br/>                                   | Lecture seule<br/>  | Le chemin d’accès complet du fichier. vmc pour la configuration de l’ordinateur virtuel.<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Lecture seule<br/>  | Collection énumérable de lecteurs de disquette attachés à la machine virtuelle.<br/>                                                          |
| [**Invité**](ivmvirtualmachine-guestos.md)<br/>                             | Lecture seule<br/>  | Le système d’exploitation invité de cet ordinateur virtuel.<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Lecture seule<br/>  | Collection énumérable de connexions de disque dur.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Lecture seule<br/>  | Indique si le processeur prend en charge le jeu d’instructions 3DNow.<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | Lecture seule<br/>  | Indique si le processeur prend en charge le jeu d’instructions MMX.<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | Lecture seule<br/>  | Indique si le processeur prend en charge le jeu d’instructions SSE.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Lecture seule<br/>  | Indique si le processeur prend en charge le jeu d’instructions SSE2.<br/>                                                                  |
| [**Clavier**](ivmvirtualmachine-keyboard.md)<br/>                           | Lecture seule<br/>  | Périphérique clavier de l’ordinateur virtuel.<br/>                                                                                        |
| [**Capacité**](ivmvirtualmachine-memory.md)<br/>                               | Lecture/écriture<br/> | Quantité de mémoire physique de l’ordinateur virtuel, en mégaoctets.<br/>                                                                 |
| [**Souris**](ivmvirtualmachine-mouse.md)<br/>                                 | Lecture seule<br/>  | Périphérique de la souris pour la machine virtuelle.<br/>                                                                                           |
| [**Nom**](ivmvirtualmachine-name.md)<br/>                                   | Lecture/écriture<br/> | Nom de la configuration de l’ordinateur virtuel.<br/>                                                                                      |
| [**NetworkAdapters**](ivmvirtualmachine-networkadapters.md)<br/>             | Lecture seule<br/>  | Collection énumérable de cartes réseau attachées à la machine virtuelle.<br/>                                                                   |
| [**Remarques**](ivmvirtualmachine-notes.md)<br/>                                 | Lecture/écriture<br/> | Remarques relatives à la machine virtuelle.<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | Lecture seule<br/>  | Collection énumérable de ports parallèles.<br/>                                                                                         |
| [**ProcessorSpeed**](ivmvirtualmachine-processorspeed.md)<br/>               | Lecture seule<br/>  | Vitesse du processeur, en mégahertz (MHz).<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | Lecture seule<br/>  | Nom de la connexion RDP nommée canal utilisé pour la vidéo et l’entrée.<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Lecture seule<br/>  | Chemin d’accès complet au fichier d’état enregistré.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Lecture seule<br/>  | Collection énumérable de ports série.<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Lecture/écriture<br/> | action à exécuter sur cet ordinateur virtuel s’il est en cours d’exécution lorsque Windows ordinateur virtuel est fermé.<br/>                                |
| [**Département**](ivmvirtualmachine-state.md)<br/>                                 | Lecture seule<br/>  | État actuel de l’ordinateur virtuel.<br/>                                                                                           |
| [**Annulable**](ivmvirtualmachine-undoable.md)<br/>                           | Lecture/écriture<br/> | Indique si les disques d’annulations sont activés pour les disques durs connectés à la machine virtuelle.<br/>                                      |
| [**UndoAction**](ivmvirtualmachine-undoaction.md)<br/>                       | Lecture/écriture<br/> | Action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est arrêtée depuis le système d’exploitation invité.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



 


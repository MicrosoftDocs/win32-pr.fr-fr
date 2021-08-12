---
title: Interface IVMGuestOS (VPCCOMInterfaces. h)
description: Définit le système d’exploitation invité en cours d’exécution au sein d’une machine virtuelle.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- Virtual PC de l’interface IVMGuestOS
- IVMGuestOS interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a36c6c579209903c45e3888a11f17d40c168bbb2e215c60fb25e5b12330962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593997"
---
# <a name="ivmguestos-interface"></a>Interface IVMGuestOS

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit le système d’exploitation invité en cours d’exécution au sein d’une machine virtuelle. Cette interface vous permet d’interagir avec les composants d’intégration qui s’exécutent dans le système d’exploitation invité. Le **IVMGuestOS** d’un ordinateur virtuel peut être récupéré à l’aide de la propriété [**IVMVirtualMachine :: guestos**](ivmvirtualmachine-guestos.md) .

## <a name="members"></a>Membres

L’interface **IVMGuestOS** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMGuestOS** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMGuestOS** possède ces méthodes.



| Méthode                                                                          | Description                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | Récupère des informations de version pour le système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | Récupère un paramètre nommé au sein de l’invité.<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | Localise et installe les derniers composants d’intégration dans le système d’exploitation invité.<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | Détermine si la session demandée est présente.<br/>                                         |
| [**Fermeture**](ivmguestos-logoff.md)                                             | Déconnecte tous les utilisateurs du système d’exploitation invité.<br/>                                          |
| [**Faire**](ivmguestos-restart.md)                                           | Redémarre le système d’exploitation invité.<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | Définit un paramètre nommé au sein de l’invité.<br/>                                                     |
| [**Correct**](ivmguestos-shutdown.md)                                         | Arrête le système d’exploitation invité.<br/>                                                       |



 

### <a name="properties"></a>Propriétés

L’interface **IVMGuestOS** possède les propriétés suivantes.



| Propriété                                                                                   | Type d’accès           | Description                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | Lecture seule<br/>  | Indique si le système d’exploitation invité peut être arrêté proprement (nécessite des composants d’intégration).<br/>                         |
| [**ComputerName**](ivmguestos-computername.md)<br/>                                 | Lecture seule<br/>  | Nom d’ordinateur du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Lecture seule<br/>  | CSDVersion du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | Lecture seule<br/>  | Pourcentage de pulsations attendues reçues au cours de la dernière minute.<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | Lecture seule<br/>  | Version des composants d’intégration installés dans le système d’exploitation invité.<br/>                                               |
| [**IsHeartbeating**](ivmguestos-isheartbeating.md)<br/>                             | Lecture seule<br/>  | Indique si la machine virtuelle a une pulsation.<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Lecture/écriture<br/> | Indique si les composants d’intégration de cet ordinateur virtuel doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte.<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Lecture seule<br/>  | Indique si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Lecture seule<br/>  | Numéro de build du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Lecture seule<br/>  | Version principale du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Lecture seule<br/>  | Version mineure du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Lecture seule<br/>  | Nom du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | Lecture seule<br/>  | Identificateur de plateforme du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Lecture seule<br/>  | Version du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Lecture seule<br/>  | Type de produit du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | Lecture seule<br/>  | Indique si l’écran est verrouillé dans le système d’exploitation invité.<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | Lecture seule<br/>  | Version principale du Service Pack du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | Lecture seule<br/>  | La version mineure du Service Pack du système d’exploitation invité s’exécutant sur la machine virtuelle.<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | Lecture seule<br/>  | SuiteMask du système d’exploitation invité en cours d’exécution sur la machine virtuelle.<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | Lecture seule<br/>  | Port utilisé par Services Bureau à distance dans le système d’exploitation invité.<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | Lecture seule<br/>  | État de l’initialisation des services Terminal Server dans le système d’exploitation invité.<br/>                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



 


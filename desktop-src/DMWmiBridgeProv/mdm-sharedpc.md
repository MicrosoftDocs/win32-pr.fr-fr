---
title: Classe MDM_SharedPC
description: La \_ classe SHAREDPC MDM est utilisée pour configurer les paramètres d’utilisation des PC partagés.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- Classe MDM_SharedPC
- Classe MDM_SharedPC, Description
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d4888e0d8129584e79124079e93459bc6d9f963fe026704f52b34de05b755e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693459"
---
# <a name="mdm_sharedpc-class"></a>\_Classe SHAREDPC MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ classe SHAREDPC MDM est utilisée pour configurer les paramètres d’utilisation des PC partagés.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a>Membres

La **classe \_ SharedPC MDM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ SharedPC MDM** a ces propriétés.

<dl> <dt>

[AccountModel](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[DeletionPolicy](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[DiskLevelCaching](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[DiskLevelDeletion](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[EnableAccountManager](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[EnableSharedPCMode](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[InactiveThreshold](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[KioskModeAUMID](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[KioskModeUserTileDisplayText](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[MaintenanceStartTime](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[MaxPageFileSizeMB](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RestrictLocalStorage](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[SetEduPolicies](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[SetPowerPolicies](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[SignInOnResume](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> <dt>

[SleepTimeout](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                       |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 


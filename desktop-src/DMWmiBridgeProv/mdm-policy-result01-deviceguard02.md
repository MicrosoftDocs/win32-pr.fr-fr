---
title: Classe MDM_Policy_Result01_DeviceGuard02
description: La \_ classe Result01 DeviceGuard02 de la stratégie MDM \_ \_ configure les stratégies Device Guard.
ms.assetid: ba21d324-85dc-4cb5-8123-196413e457eb
keywords:
- Classe MDM_Policy_Result01_DeviceGuard02
- Classe MDM_Policy_Result01_DeviceGuard02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceGuard02
- MDM_Policy_Result01_DeviceGuard02.InstanceID
- MDM_Policy_Result01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e206a732628e442a391cb8b29f7712f5a5ec8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032596"
---
# <a name="mdm_policy_result01_deviceguard02-class"></a>\_Classe DeviceGuard02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ classe Result01 DeviceGuard02 de la stratégie MDM \_ \_ configure les stratégies Device Guard.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ DeviceGuard02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ DeviceGuard02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[EnableVirtualizationBasedSecurity](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

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

[LsaCfgFlags](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

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

[RequirePlatformSecurityFeatures](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


---
title: Classe MDM_Policy_Config01_Kerberos02
description: La \_ classe Config01 Kerberos02 de la stratégie MDM \_ \_ configure les stratégies Kerberos.
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- Classe MDM_Policy_Config01_Kerberos02
- Classe MDM_Policy_Config01_Kerberos02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a0d0e0c1dfe1e1f4969c99a449332ba856a28793c5575837f8953754343a7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077133"
---
# <a name="mdm_policy_config01_kerberos02-class"></a>\_Classe Kerberos02 de la stratégie MDM \_ Config01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ classe Config01 Kerberos02 de la stratégie MDM \_ \_ configure les stratégies Kerberos.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Config01 \_ Kerberos02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Config01 \_ Kerberos02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[AllowForestSearchOrder](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

[KerberosClientSupportsClaimsCompoundArmor](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

[RequireKerberosArmoring](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[RequireStrictKDCValidation](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[SetMaximumContextTokenSize](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


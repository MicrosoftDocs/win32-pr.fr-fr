---
title: Classe MDM_Policy_Result01_ApplicationDefaults02
description: La \_ classe Result01 ApplicationDefaults02 de la stratégie MDM \_ \_ représente les stratégies de paramètres par défaut de l’application disponibles.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- Classe MDM_Policy_Result01_ApplicationDefaults02
- Classe MDM_Policy_Result01_ApplicationDefaults02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842a80517234ba0aa2bdfbca5330c9b4b22cd98024651bdd650b2e43d847cae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164809"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a>\_Classe ApplicationDefaults02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ classe Result01 ApplicationDefaults02 de la stratégie MDM \_ \_ représente les stratégies de paramètres par défaut de l’application disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ ApplicationDefaults02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ ApplicationDefaults02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
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

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
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



 


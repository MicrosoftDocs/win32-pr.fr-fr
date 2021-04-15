---
title: Classe MDM_Policy_Result01_LockDown02
description: La \_ classe Result01 Lockdown02 de la stratégie MDM \_ \_ représente les stratégies de verrouillage disponibles.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- Classe MDM_Policy_Result01_LockDown02
- Classe MDM_Policy_Result01_LockDown02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465011"
---
# <a name="mdm_policy_result01_lockdown02-class"></a>\_Classe LockDown02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Result01 \_ Lockdown02 de la stratégie MDM** représente les stratégies de verrouillage disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ LockDown02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ LockDown02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[AllowEdgeSwipe](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « Lockdown ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 


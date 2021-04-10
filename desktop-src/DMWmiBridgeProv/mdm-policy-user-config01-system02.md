---
title: Classe MDM_Policy_User_Config01_System02
description: La \_ \_ classe Config01 System02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de télémétrie disponibles.
ms.assetid: 3f049152-6868-4b10-8711-dadc4cb012b4
keywords:
- Classe MDM_Policy_User_Config01_System02
- Classe MDM_Policy_User_Config01_System02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_System02
- MDM_Policy_User_Config01_System02.InstanceID
- MDM_Policy_User_Config01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eefa8a08320b79c80d4e0cb359fd1194a21ae4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103861"
---
# <a name="mdm_policy_user_config01_system02-class"></a>Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ System02

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ \_ classe Config01 System02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de télémétrie disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTelemetry;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ \_ Config01 \_ System02 de la stratégie MDM User** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ \_ Config01 \_ System02 de la stratégie MDM User** a ces propriétés.

<dl> <dt>

[AllowTelemetry](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


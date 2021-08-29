---
title: Classe MDM_Policy_User_Result01_Authentication02
description: La \_ \_ classe Result01 Authentication02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de gestion des authentifications disponibles.
ms.assetid: 57da7a17-9955-445d-998e-369b101cda3c
keywords:
- Classe MDM_Policy_User_Result01_Authentication02
- Classe MDM_Policy_User_Result01_Authentication02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Authentication02
- MDM_Policy_User_Result01_Authentication02.InstanceID
- MDM_Policy_User_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2f0864f32aabd257facdef5f5dbe64c78fd6d7d69241be509057187e8e8645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693759"
---
# <a name="mdm_policy_user_result01_authentication02-class"></a>Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ Authentication02

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ \_ Result01 \_ Authentication02 utilisateur de la stratégie MDM** représente les stratégies de gestion des authentifications disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEAPCertSSO;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ \_ Result01 \_ Authentication02 de la stratégie MDM User** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ \_ Result01 \_ Authentication02 de la stratégie MDM User** a ces propriétés.

<dl> <dt>

[AllowEAPCertSSO](/windows/client-management/mdm/policy-csp-authentication#authentication-alloweapcertsso)
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « Authentication ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./User/Vendor/MSFT/Policy/Result »

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


---
title: Classe MDM_Policy_User_Config01_Desktop02
description: La \_ \_ classe Config01 Desktop02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de profil de dossier disponibles.
ms.assetid: 44a60c60-bae5-44b2-b096-387c915e2692
keywords:
- Classe MDM_Policy_User_Config01_Desktop02
- Classe MDM_Policy_User_Config01_Desktop02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Desktop02
- MDM_Policy_User_Config01_Desktop02.InstanceID
- MDM_Policy_User_Config01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f4ef08329b3927d7e3c3328c7c2f033fb25026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843285"
---
# <a name="mdm_policy_user_config01_desktop02-class"></a>Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ Desktop02

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ \_ classe Config01 Desktop02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de profil de dossier disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ \_ Config01 \_ Desktop02 de la stratégie MDM User** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ \_ Config01 \_ Desktop02 de la stratégie MDM User** a ces propriétés.

<dl> <dt>

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

</dd> <dt>

[PreventUserRedirectionOfProfileFolders](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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



 


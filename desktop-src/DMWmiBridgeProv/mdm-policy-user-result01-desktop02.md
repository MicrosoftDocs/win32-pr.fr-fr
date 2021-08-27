---
title: Classe MDM_Policy_User_Result01_Desktop02
description: La \_ \_ classe Result01 Desktop02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de profil de dossier disponibles.
ms.assetid: dab89ac4-b857-474e-8fe5-6822fe06ac91
keywords:
- Classe MDM_Policy_User_Result01_Desktop02
- Classe MDM_Policy_User_Result01_Desktop02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02.InstanceID
- MDM_Policy_User_Result01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a8628cc30c5ababe6cd6f0620bb09fad336f44fc8846725c15234a141e1a09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131879"
---
# <a name="mdm_policy_user_result01_desktop02-class"></a>Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ Desktop02

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La \_ \_ classe Result01 Desktop02 utilisateur de la stratégie MDM \_ \_ représente les stratégies de profil de dossier disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ \_ Result01 \_ Desktop02 de la stratégie MDM User** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ \_ Result01 \_ Desktop02 de la stratégie MDM User** a ces propriétés.

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


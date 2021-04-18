---
title: Classe MDM_Policy_Config01_ActiveXControls02
description: Ce paramètre de stratégie détermine les sites d’installation ActiveX que les utilisateurs standard de votre organisation peuvent utiliser pour installer des contrôles ActiveX sur leurs ordinateurs.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- Classe MDM_Policy_Config01_ActiveXControls02
- Classe MDM_Policy_Config01_ActiveXControls02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512566"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a>\_Classe ActiveXControls02 de la stratégie MDM \_ Config01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Ce paramètre de stratégie détermine les sites d’installation ActiveX que les utilisateurs standard de votre organisation peuvent utiliser pour installer des contrôles ActiveX sur leurs ordinateurs. Lorsque ce paramètre est activé, l’administrateur peut créer une liste des sites d’installation ActiveX approuvés spécifiés par l’URL de l’hôte.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Config01 \_ ActiveXControls02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Config01 \_ ActiveXControls02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[ApprovedInstallationSites](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 


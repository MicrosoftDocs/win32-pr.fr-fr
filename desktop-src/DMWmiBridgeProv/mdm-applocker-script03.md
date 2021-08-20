---
title: Classe MDM_AppLocker_Script03
description: La \_ \_ classe SCRIPT03 de MDM AppLocker définit les restrictions de stratégie pour le traitement des fichiers dll.
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- Classe MDM_AppLocker_Script03
- Classe MDM_AppLocker_Script03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681b70e98352bae70decf4d94dd78a2a08a1e180713056d37593c540896f2b86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077343"
---
# <a name="mdm_applocker_script03-class"></a>\_ \_ Classe SCRIPT03 de MDM AppLocker

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Script03 de MDM AppLocker** définit les restrictions de stratégie pour le traitement des fichiers dll.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Script03 de MDM AppLocker** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Script03 de MDM AppLocker** a ces propriétés.

<dl> <dt>

[**EnforcementMode**](/windows/client-management/mdm/applocker-csp)
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

Identifie le nom du nœud parent.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions »

</dd> <dt>

[**Policy**](/windows/client-management/mdm/applocker-csp)
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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


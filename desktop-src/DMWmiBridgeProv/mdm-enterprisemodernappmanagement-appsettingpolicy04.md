---
title: Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: La \_ classe EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM spécifie toutes les valeurs de paramètre d’application gérée.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba82be4653266c94465917857eb47b014399594525a6f0f18264e4f73651684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077253"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a>\_ \_ Classe APPSETTINGPOLICY04 EnterpriseModernAppManagement MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** spécifie toutes les valeurs de paramètre d’application gérée.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a>Membres

La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ EnterpriseModernAppManagement \_ AppSettingPolicy04 MDM** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne « AppSettingPolicy ».

</dd> <dt>

[IsVariableLeaf](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

ajouté dans Windows 10, version 1511. Les **SettingValue** et les données représentent une paire clé-valeur à configurer pour l’application. Le nœud représente le nom de la clé et les données représentent la valeur. Vous pouvez trouver cette valeur dans LocalSettings dans le Managed.App. conteneur Paramètres.

Ce paramètre ne fonctionne que pour les applications qui prennent en charge la fonctionnalité et qui sont uniquement prises en charge dans le contexte de l’utilisateur.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*»

</dd> <dt>

[**Valeur**](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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

 


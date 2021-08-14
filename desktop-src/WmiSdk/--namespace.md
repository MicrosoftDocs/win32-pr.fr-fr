---
description: Représente un espace de noms WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320767"
---
# <a name="__namespace-class"></a>\_\_Classe d’espace de noms

La classe de système d' **\_ \_ espace de noms** représente un espace de noms WMI.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Membres

La classe d' **\_ \_ espace de noms** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ \_ espace de noms** a ces propriétés.

<dl> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Nom de l’espace de noms.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe d' **\_ \_ espace de noms** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.

Vous pouvez utiliser l' **\_ \_ espace de noms** pour identifier, créer et supprimer des espaces de noms enfants dans l’espace de noms de travail actuel pour lequel vous avez un objet [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . La création d’une nouvelle instance d' **\_ \_ espace de noms** dans un espace de noms de travail crée un espace de noms enfant dans l’espace de noms de travail. À l’inverse, la suppression d’une instance d' **\_ \_ espace de noms** supprime l’espace de noms enfant de l’espace de noms de travail. Notez que la suppression d’un espace de noms enfant supprime également toutes ses classes et instances.

L’énumération des instances de cette classe dans n’importe quel espace de noms de travail donne les espaces de noms enfants disponibles.

Par exemple, dans l' \\ espace de noms racine se trouvent deux instances d' **\_ \_ espace de noms**. La propriété **Name** est définie sur « Default », l' **autre est définie** sur « Cimv2 ». Ces instances représentent \\ \\ , respectivement, les espaces de noms root par défaut et \\ root \\ cimv2.

## <a name="examples"></a>Exemples

L’exemple VBScript [répertorier tous les espaces de noms WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) dans la Galerie TechNet utilise un appel récursif pour répertorier toutes les instances de la \_ \_ classe d’espace de noms sur un système.

L’exemple de code suivant récupère tous les espaces de noms dans PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



L’exemple de code suivant améliore l’exemple précédent et ajoute des informations supplémentaires.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

 





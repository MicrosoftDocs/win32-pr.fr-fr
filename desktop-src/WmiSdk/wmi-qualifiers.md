---
description: WMI a plusieurs types de qualificateurs de classe et de propriété. Les qualificateurs peuvent également avoir des variantes de modification.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Qualificateurs WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf51888592949aadefec7c864dc0a24df6a4fa68f6fb34c8e3cda880da6873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502809"
---
# <a name="wmi-qualifiers"></a>Qualificateurs WMI

WMI a plusieurs types de [*qualificateurs*](gloss-q.md)de classe et de propriété. Les qualificateurs peuvent également avoir des [*variantes*](gloss-f.md)de modification. Les types de qualificateurs et de versions suivants sont utilisés dans WMI.

Le nom de chaque qualificateur apparaît avec son type de données et indique si le qualificateur peut être appliqué à une classe, une instance, une propriété ou une méthode. Pour les qualificateurs tels que l' **Association** (abordé sous les [qualificateurs Meta](meta-qualifiers.md)), il existe une règle d’utilisation implicite qui doit également être présente dans le qualificateur meta. Par exemple, la règle d’utilisation implicite pour les qualificateurs d' **agrégation** est que le qualificateur d' **Association** doit également être présent.



| Type de qualificateur                              | Description                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [METADONNEES](meta-qualifiers.md)                 | Affine la définition des méta-constructions en clarifiant l’utilisation réelle d’une déclaration de classe ou de propriété.                          |
| [Facultatif](optional-qualifiers.md)         | Traite les situations non communes à toutes les implémentations compatibles CIM.                                                                 |
| [Types de qualificateurs](qualifier-flavors.md)  | Fournit des informations supplémentaires sur un qualificateur, par exemple si une classe ou une instance dérivée peut substituer la valeur d’origine du qualificateur. |
| [Standard](standard-qualifiers.md)         | Prend en charge les descriptions que toutes les implémentations compatibles CIM doivent gérer.                                                         |
| [Spécifique à WMI](wmi-specific-qualifiers.md) | Décrit les qualificateurs spécifiques à WMI, tels que les qualificateurs de classe du compteur de performance.                                                   |



 

Pour plus d’informations sur l’application de qualificateurs à vos classes WMI, consultez [Ajout d’un qualificateur](adding-a-qualifier.md). Pour voir comment examiner des qualificateurs sur des classes WMI existantes, consultez l’exemple de code ci-dessous.

## <a name="example"></a>Exemples

Le code PowerShell suivant, tiré de la [Galerie TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), explique comment récupérer des qualificateurs d’une classe WMI.


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 




---
description: La rubrique suivante explique comment récupérer la documentation de programmation en ligne pour un objet de données brutes ou mis en forme créé dynamiquement.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Récupération de la documentation pour les objets de données de performance bruts et mis en forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320673"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Récupération de la documentation pour les objets de données de performance bruts et mis en forme

La rubrique suivante explique comment récupérer la documentation de programmation en ligne pour un objet de données brutes ou mis en forme créé dynamiquement.

WMI contient un certain nombre d’objets qui effectuent le suivi des performances. Les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contiennent des données de performances brutes, ou « décuites », et sont prises en charge par le [fournisseur de compteurs de performance](performance-counter-provider.md). En revanche, les classes dérivées de [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent des données mises en forme « cuites », et sont prises en charge par le [fournisseur de données de performance mis en forme](formatted-performance-data-provider.md).

Toutefois, les deux fournisseurs prennent en charge un certain nombre de classes enfants créées dynamiquement. Étant donné que les propriétés sont ajoutées au moment de l’exécution, ces classes peuvent contenir des propriétés non documentées. Vous pouvez utiliser le code suivant pour identifier les propriétés d’une classe créée dynamiquement.

**Pour récupérer une description d’une classe créée dynamiquement**

1.  Créez une instance de l’élément et affectez la valeur true au qualificateur modifié.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Récupérez les propriétés de la classe.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Affichez les propriétés.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

Le code suivant récupère les descriptions de propriété pour l’objet [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) spécifié.


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 

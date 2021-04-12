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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="22ea2-103">Récupération de la documentation pour les objets de données de performance bruts et mis en forme</span><span class="sxs-lookup"><span data-stu-id="22ea2-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="22ea2-104">La rubrique suivante explique comment récupérer la documentation de programmation en ligne pour un objet de données brutes ou mis en forme créé dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="22ea2-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="22ea2-105">WMI contient un certain nombre d’objets qui effectuent le suivi des performances.</span><span class="sxs-lookup"><span data-stu-id="22ea2-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="22ea2-106">Les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contiennent des données de performances brutes, ou « décuites », et sont prises en charge par le [fournisseur de compteurs de performance](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22ea2-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="22ea2-107">En revanche, les classes dérivées de [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent des données mises en forme « cuites », et sont prises en charge par le [fournisseur de données de performance mis en forme](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22ea2-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="22ea2-108">Toutefois, les deux fournisseurs prennent en charge un certain nombre de classes enfants créées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="22ea2-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="22ea2-109">Étant donné que les propriétés sont ajoutées au moment de l’exécution, ces classes peuvent contenir des propriétés non documentées.</span><span class="sxs-lookup"><span data-stu-id="22ea2-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="22ea2-110">Vous pouvez utiliser le code suivant pour identifier les propriétés d’une classe créée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="22ea2-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="22ea2-111">**Pour récupérer une description d’une classe créée dynamiquement**</span><span class="sxs-lookup"><span data-stu-id="22ea2-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="22ea2-112">Créez une instance de l’élément et affectez la valeur true au qualificateur modifié.</span><span class="sxs-lookup"><span data-stu-id="22ea2-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="22ea2-113">Récupérez les propriétés de la classe.</span><span class="sxs-lookup"><span data-stu-id="22ea2-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="22ea2-114">Affichez les propriétés.</span><span class="sxs-lookup"><span data-stu-id="22ea2-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="22ea2-115">Le code suivant récupère les descriptions de propriété pour l’objet [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) spécifié.</span><span class="sxs-lookup"><span data-stu-id="22ea2-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


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



 

 

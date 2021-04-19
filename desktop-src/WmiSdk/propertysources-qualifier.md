---
description: Chaque propriété d’une classe d’affichage doit avoir un qualificateur de tableau de chaînes appelé PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificateur PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524936"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="4d583-103">Qualificateur PropertySources</span><span class="sxs-lookup"><span data-stu-id="4d583-103">PropertySources Qualifier</span></span>

<span data-ttu-id="4d583-104">Chaque propriété d’une classe d’affichage doit avoir un qualificateur de tableau de chaînes appelé **PropertySources**.</span><span class="sxs-lookup"><span data-stu-id="4d583-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="4d583-105">Le qualificateur **PropertySources** contient le nom de la ou des propriétés de classe source à partir desquelles cette propriété de la classe de vue obtient des données.</span><span class="sxs-lookup"><span data-stu-id="4d583-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="4d583-106">L’ordre des valeurs de ce tableau correspond à l’ordre des classes sources définies pour le [qualificateur ViewSources](viewsources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="4d583-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="4d583-107">L’exemple suivant montre comment définir une propriété pour une classe d’affichage d’Union qui est l’Union de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) à partir de deux ordinateurs différents :</span><span class="sxs-lookup"><span data-stu-id="4d583-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="4d583-108">La première propriété **DeviceID** correspond à la propriété **DeviceID** de la classe dans la première requête source.</span><span class="sxs-lookup"><span data-stu-id="4d583-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="4d583-109">La deuxième propriété **DeviceID** est la propriété **DeviceID** de la classe dans la deuxième requête source.</span><span class="sxs-lookup"><span data-stu-id="4d583-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="4d583-110">Lors de la définition des propriétés des classes de vue de jointure, vous devez définir une propriété de vue distincte pour chacune des propriétés de la classe source, sauf si les propriétés de la classe source sont la base de la classe de vue de jointure.</span><span class="sxs-lookup"><span data-stu-id="4d583-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="4d583-111">L’exemple suivant crée des propriétés dans une classe de vue de jointure sur des propriétés similaires de la classe source [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et de la classe source [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="4d583-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="4d583-112">Si les deux classes sources sont jointes par une propriété commune, vous ne pouvez définir qu’une seule propriété de classe d’affichage, car la valeur des deux propriétés de la classe source est toujours la même.</span><span class="sxs-lookup"><span data-stu-id="4d583-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="4d583-113">L’exemple suivant montre comment joindre la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) par une valeur de propriété commune :</span><span class="sxs-lookup"><span data-stu-id="4d583-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="4d583-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d583-114">Requirements</span></span>



| <span data-ttu-id="4d583-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d583-115">Requirement</span></span> | <span data-ttu-id="4d583-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d583-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4d583-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d583-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d583-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d583-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4d583-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d583-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d583-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d583-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d583-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d583-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d583-122">**Qualificateurs spécifiques au fournisseur de vues**</span><span class="sxs-lookup"><span data-stu-id="4d583-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 


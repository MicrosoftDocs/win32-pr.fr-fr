---
description: Désactive la possibilité d’épingler un raccourci ou une fenêtre dans la barre des tâches ou dans le menu Démarrer. Cette propriété rend également l’élément inéligible pour l’inclusion dans la liste des plus fréquemment utilisés (MFU) du menu Démarrer.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865565"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="f6fd7-104">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="f6fd7-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="f6fd7-105">Désactive la possibilité d’épingler un raccourci ou une fenêtre dans la barre des tâches ou dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="f6fd7-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="f6fd7-106">Cette propriété rend également l’élément inéligible pour l’inclusion dans la liste des plus fréquemment utilisés (MFU) du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="f6fd7-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="f6fd7-107">Cette propriété doit être définie sur une fenêtre avant la propriété de l’ID de groupe de [ \_ \_ sécurité AppUserModel](./props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fd7-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="f6fd7-108">Une fois que \_ la \_ propriété ID de la AppUserModel de la valeur du groupe [de \_ \_ ]() sécurité</span><span class="sxs-lookup"><span data-stu-id="f6fd7-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="f6fd7-109">Pour plus d’informations sur les ID de modèle d’utilisateur d’application (AppUserModelIDs) et d’autres méthodes d’exclusion d’un élément de l’épinglage à la barre des tâches et de l’inclusion MFU, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="f6fd7-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="f6fd7-110">Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. PreventPinning]() de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f6fd7-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="f6fd7-111">La définition de cette propriété entraîne l’ignorance des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f6fd7-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="f6fd7-112">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="f6fd7-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="f6fd7-113">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="f6fd7-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="f6fd7-114">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="f6fd7-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="f6fd7-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6fd7-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="f6fd7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f6fd7-116">Remarks</span></span>

<span data-ttu-id="f6fd7-117">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="f6fd7-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6fd7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6fd7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6fd7-119">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="f6fd7-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="f6fd7-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="f6fd7-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="f6fd7-122">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="f6fd7-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f6fd7-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f6fd7-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f6fd7-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="f6fd7-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f6fd7-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f6fd7-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-134">variables</span><span class="sxs-lookup"><span data-stu-id="f6fd7-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-135">enumRange</span><span class="sxs-lookup"><span data-stu-id="f6fd7-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-136">image</span><span class="sxs-lookup"><span data-stu-id="f6fd7-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="f6fd7-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-138">editControl</span><span class="sxs-lookup"><span data-stu-id="f6fd7-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="f6fd7-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="f6fd7-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-141">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="f6fd7-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="f6fd7-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="f6fd7-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 

---
description: Empêche une entrée de menu Démarrer pour un raccourci d’application récemment installé de recevoir une surbrillance.
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: System. AppUserModel. ExcludeFromShowInNewInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206cbbc6b07b0d3fec5833c046d4cb44c1e5e4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519719"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a><span data-ttu-id="0dcd0-103">System. AppUserModel. ExcludeFromShowInNewInstall</span><span class="sxs-lookup"><span data-stu-id="0dcd0-103">System.AppUserModel.ExcludeFromShowInNewInstall</span></span>

<span data-ttu-id="0dcd0-104">Empêche une entrée de menu **Démarrer** pour un raccourci d’application récemment installé de recevoir une surbrillance.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-104">Prevents a **Start** menu entry for a newly installed application shortcut from receiving a highlight.</span></span> <span data-ttu-id="0dcd0-105">Cela revient à désactiver l’option **mettre en surbrillance les programmes récemment installés** dans la fenêtre **personnaliser le menu Démarrer** sur un élément individuel.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-105">This is equivalent to clearing the **Highlight newly installed programs** option in the **Customize Start Menu** window on an individual item.</span></span> <span data-ttu-id="0dcd0-106">Cette propriété doit être définie sur les raccourcis pour les outils et les applications secondaires.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-106">This property should be set on shortcuts for tools and secondary applications.</span></span>

> [!Note]  
> <span data-ttu-id="0dcd0-107">Cette propriété est utilisée uniquement par le menu Démarrer sur Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-107">This property is property is only used by the Start menu on Windows Vista and Windows 7.</span></span> <span data-ttu-id="0dcd0-108">La propriété n’est pas utilisée par l’écran de démarrage ou le menu Démarrer sur Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0dcd0-108">The property is not used by the Start screen or Start menu on Windows 8 and later</span></span>

 

<span data-ttu-id="0dcd0-109">.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-109">.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="0dcd0-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0dcd0-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="0dcd0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0dcd0-111">Remarks</span></span>

<span data-ttu-id="0dcd0-112">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dcd0-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0dcd0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dcd0-114">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="0dcd0-114">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-115">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="0dcd0-115">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-116">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="0dcd0-116">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="0dcd0-117">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="0dcd0-117">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-118">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0dcd0-118">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-119">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-119">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-120">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-120">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-121">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-121">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-122">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-122">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-123">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-123">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0dcd0-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0dcd0-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-126">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0dcd0-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0dcd0-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0dcd0-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-129">variables</span><span class="sxs-lookup"><span data-stu-id="0dcd0-129">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-130">enumRange</span><span class="sxs-lookup"><span data-stu-id="0dcd0-130">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-131">image</span><span class="sxs-lookup"><span data-stu-id="0dcd0-131">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-132">drawControl</span><span class="sxs-lookup"><span data-stu-id="0dcd0-132">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-133">editControl</span><span class="sxs-lookup"><span data-stu-id="0dcd0-133">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-134">filterControl</span><span class="sxs-lookup"><span data-stu-id="0dcd0-134">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-135">queryControl</span><span class="sxs-lookup"><span data-stu-id="0dcd0-135">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-136">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="0dcd0-136">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="0dcd0-137">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="0dcd0-137">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> <dt>

<span data-ttu-id="0dcd0-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0dcd0-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span></span>
</dt> </dl>

 

 

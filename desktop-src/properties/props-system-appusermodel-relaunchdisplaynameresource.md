---
description: Spécifie le nom complet utilisé pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104202936"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="eeb12-103">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="eeb12-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="eeb12-104">Spécifie le nom complet utilisé pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.</span><span class="sxs-lookup"><span data-stu-id="eeb12-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="eeb12-105">La valeur de cette propriété doit être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="eeb12-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="eeb12-106">Une chaîne de ressource indirecte telle que « @% systemdir% \\ system32 \\shell32.dll,-19263 ».</span><span class="sxs-lookup"><span data-stu-id="eeb12-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="eeb12-107">Notez que le caractère « @ » est requis pour distinguer une chaîne indirecte d’une chaîne de texte brut (décrite dans le paragraphe à puces suivant).</span><span class="sxs-lookup"><span data-stu-id="eeb12-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="eeb12-108">Cette chaîne indirecte se compose d’un fichier binaire et d’un ID de ressource de la chaîne contenue dans ce binaire.</span><span class="sxs-lookup"><span data-stu-id="eeb12-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="eeb12-109">Nous vous recommandons vivement d’utiliser ce format de chaîne indirecte, qui garantit que le nom d’affichage change de manière appropriée lorsque la langue du système est modifiée par le biais de l’interface utilisateur multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="eeb12-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="eeb12-110">Le caractère « - » avant l’ID de ressource est requis.</span><span class="sxs-lookup"><span data-stu-id="eeb12-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="eeb12-111">Chaîne de texte brut qui ne pointe pas vers une ressource.</span><span class="sxs-lookup"><span data-stu-id="eeb12-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="eeb12-112">Cela doit être utilisé uniquement lorsque le nom complet est calculé dynamiquement ou obtenu à partir d’une source de données qui ne prend pas en charge MUI.</span><span class="sxs-lookup"><span data-stu-id="eeb12-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="eeb12-113">Par exemple, la chaîne peut être le nom d’un périphérique, tel que « Microsoft Zune », dans les cas où l’application s’affiche lorsque l’appareil est connecté à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eeb12-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="eeb12-114">[System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) et [System. AppUserModel. RelaunchDisplayNameResource]() doivent toujours être définis ensemble.</span><span class="sxs-lookup"><span data-stu-id="eeb12-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="eeb12-115">Si l’une de ces propriétés n’est pas définie, aucune n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="eeb12-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="eeb12-116">Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="eeb12-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="eeb12-117">Si la fenêtre n’a pas de AppUserModelID explicite, cette propriété est ignorée et la fenêtre est regroupée et épinglée comme s’il s’agissait d’une partie du processus qui le possède.</span><span class="sxs-lookup"><span data-stu-id="eeb12-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="eeb12-118">Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="eeb12-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="eeb12-119">Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut.</span><span class="sxs-lookup"><span data-stu-id="eeb12-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="eeb12-120">Pour plus d’informations, consultez [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="eeb12-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="eeb12-121">Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="eeb12-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="eeb12-122">Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.</span><span class="sxs-lookup"><span data-stu-id="eeb12-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="eeb12-123">Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchDisplayNameResource]() de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="eeb12-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="eeb12-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="eeb12-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="eeb12-125">Notes</span><span class="sxs-lookup"><span data-stu-id="eeb12-125">Remarks</span></span>

<span data-ttu-id="eeb12-126">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="eeb12-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeb12-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eeb12-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeb12-128">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="eeb12-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="eeb12-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="eeb12-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="eeb12-130">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="eeb12-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="eeb12-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="eeb12-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="eeb12-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="eeb12-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="eeb12-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="eeb12-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="eeb12-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="eeb12-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="eeb12-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="eeb12-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="eeb12-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="eeb12-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="eeb12-142">variables</span><span class="sxs-lookup"><span data-stu-id="eeb12-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="eeb12-143">enumRange</span><span class="sxs-lookup"><span data-stu-id="eeb12-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="eeb12-144">image</span><span class="sxs-lookup"><span data-stu-id="eeb12-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="eeb12-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="eeb12-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="eeb12-146">editControl</span><span class="sxs-lookup"><span data-stu-id="eeb12-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="eeb12-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="eeb12-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="eeb12-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="eeb12-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="eeb12-149">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="eeb12-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="eeb12-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="eeb12-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 

---
description: Spécifie l’icône utilisée pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539080"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="fd44d-103">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="fd44d-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="fd44d-104">Spécifie l’icône utilisée pour le raccourci créé dans la barre des tâches lorsque l’utilisateur choisit d’épingler une application à la barre des tâches ou de lancer une nouvelle instance via la liste de raccourcis de son bouton.</span><span class="sxs-lookup"><span data-stu-id="fd44d-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="fd44d-105">Il s’agit de l’icône utilisée pour le groupe de la barre des tâches et est affichée pour une application épinglée, que cette application soit en cours d’exécution ou non.</span><span class="sxs-lookup"><span data-stu-id="fd44d-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="fd44d-106">Il doit être spécifié dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="fd44d-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="fd44d-107">Format de ressource standard, par exemple « % systemdir% \\ system32 \\shell32.dll,-128 ».</span><span class="sxs-lookup"><span data-stu-id="fd44d-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="fd44d-108">Le caractère « - » avant l’ID de ressource est requis.</span><span class="sxs-lookup"><span data-stu-id="fd44d-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="fd44d-109">N’utilisez pas le caractère « @ » au début de la chaîne du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="fd44d-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="fd44d-110">Chemin d’accès direct à un fichier d’icône, tel que "% ProgramFiles% \\ Microsoft \\ Notepad \\ . ico, 0".</span><span class="sxs-lookup"><span data-stu-id="fd44d-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="fd44d-111">Notez que dans la mesure où les fichiers. ico peuvent contenir plusieurs ressources d’icône, un ID de ressource est requis dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="fd44d-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="fd44d-112">Si le fichier. ico est une image unique, utilisez « 0 » (sans le caractère « - ») comme ID de ressource.</span><span class="sxs-lookup"><span data-stu-id="fd44d-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="fd44d-113">[System. AppUserModel. RelaunchIconResource]() est une propriété facultative.</span><span class="sxs-lookup"><span data-stu-id="fd44d-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="fd44d-114">S’il n’est pas défini, l’icône de la cible de la commande relancer ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd44d-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="fd44d-115">Toutefois, étant donné que cela peut entraîner des résultats indésirables, nous vous encourageons vivement à fournir une icône de manière explicite par le biais de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="fd44d-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="fd44d-116">Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="fd44d-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="fd44d-117">Si la fenêtre n’a pas de AppUserModelID explicite (System.AppUserModel.ID), cette propriété est ignorée et la fenêtre est regroupée et épinglée comme si elle faisaient partie de son processus propriétaire.</span><span class="sxs-lookup"><span data-stu-id="fd44d-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="fd44d-118">Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="fd44d-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="fd44d-119">Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd44d-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="fd44d-120">Pour plus d’informations, consultez [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="fd44d-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="fd44d-121">Si une valeur AppUserModelID explicite est définie sur la fenêtre, mais que cette propriété n’est pas définie, le système tente de trouver un raccourci avec la même valeur AppUserModelID et épingle ce raccourci à la barre des tâches pour représenter la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fd44d-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="fd44d-122">Si ce raccourci ne peut pas être trouvé, l’exécutable de sauvegarde du processus qui le possède est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fd44d-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="fd44d-123">Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="fd44d-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="fd44d-124">Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.</span><span class="sxs-lookup"><span data-stu-id="fd44d-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="fd44d-125">Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchIconResource]() de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fd44d-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="fd44d-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd44d-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="fd44d-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd44d-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="fd44d-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd44d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd44d-129">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="fd44d-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="fd44d-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="fd44d-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="fd44d-131">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="fd44d-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="fd44d-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="fd44d-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fd44d-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fd44d-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fd44d-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="fd44d-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fd44d-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="fd44d-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fd44d-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fd44d-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fd44d-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fd44d-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fd44d-143">variables</span><span class="sxs-lookup"><span data-stu-id="fd44d-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="fd44d-144">enumRange</span><span class="sxs-lookup"><span data-stu-id="fd44d-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="fd44d-145">image</span><span class="sxs-lookup"><span data-stu-id="fd44d-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="fd44d-146">drawControl</span><span class="sxs-lookup"><span data-stu-id="fd44d-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd44d-147">editControl</span><span class="sxs-lookup"><span data-stu-id="fd44d-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd44d-148">filterControl</span><span class="sxs-lookup"><span data-stu-id="fd44d-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fd44d-149">queryControl</span><span class="sxs-lookup"><span data-stu-id="fd44d-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="fd44d-150">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="fd44d-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="fd44d-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="fd44d-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 

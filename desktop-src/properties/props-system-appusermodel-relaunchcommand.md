---
description: Spécifie une commande qui peut être exécutée via ShellExecute pour lancer une application lorsqu’elle est épinglée à la barre des tâches ou lorsqu’une nouvelle instance de l’application est lancée par le biais de la liste de raccourcis de l’application.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520482"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="16342-103">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="16342-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="16342-104">Spécifie une commande qui peut être exécutée via [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour lancer une application lorsqu’elle est épinglée à la barre des tâches ou lorsqu’une nouvelle instance de l’application est lancée par le biais de la liste de raccourcis de l’application.</span><span class="sxs-lookup"><span data-stu-id="16342-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="16342-105">En voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="16342-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="16342-106">Cette propriété est utilisée uniquement si une fenêtre a un ID de modèle utilisateur d’application explicite (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), défini à [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="16342-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="16342-107">Si la fenêtre n’a pas de AppUserModelID explicite, cette propriété est ignorée et la fenêtre est regroupée et épinglée comme s’il s’agissait d’une partie du processus qui le possède.</span><span class="sxs-lookup"><span data-stu-id="16342-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="16342-108">Pour plus d’informations sur l’application d’un AppUserModelIDs explicite et son effet sur l’épinglage de la barre des tâches, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="16342-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="16342-109">Cette propriété est destinée à être utilisée par des applications ou des fenêtres qui souhaitent fournir des informations de redémarrage autres que celles par défaut.</span><span class="sxs-lookup"><span data-stu-id="16342-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="16342-110">[System. AppUserModel. RelaunchCommand]() et [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) doivent toujours être définis ensemble.</span><span class="sxs-lookup"><span data-stu-id="16342-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="16342-111">Si l’une de ces propriétés n’est pas définie, aucune n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="16342-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="16342-112">Cette propriété, associée à [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) et [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) , peut être utilisée pour définir visuellement une fenêtre en tant qu’application pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16342-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="16342-113">Cela est utile pour les scénarios d’application hôte, où une seule instance d’hôte exécute plusieurs applications enfants.</span><span class="sxs-lookup"><span data-stu-id="16342-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="16342-114">Par exemple, un ordinateur virtuel qui héberge plusieurs applications virtualisées peut souhaiter que ces applications virtualisées apparaissent en tant qu’applications individuelles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16342-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="16342-115">L’ordinateur virtuel peut étiqueter chaque fenêtre avec un AppUserModelID explicite et les propriétés de relancement appropriées pour les faire apparaître en tant qu’applications.</span><span class="sxs-lookup"><span data-stu-id="16342-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="16342-116">L’utilisateur peut ensuite les épingler à la barre des tâches et « relancer » l’instance épinglée.</span><span class="sxs-lookup"><span data-stu-id="16342-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="16342-117">Cette propriété est ignorée si [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) est défini.</span><span class="sxs-lookup"><span data-stu-id="16342-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="16342-118">Cela permet à une application de contrôler le regroupement de ses fenêtres en leur assignant des AppUserModelIDs explicites, mais en empêchant l’épinglage de ces fenêtres.</span><span class="sxs-lookup"><span data-stu-id="16342-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="16342-119">Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System. AppUserModel. RelaunchCommand]() de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="16342-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="16342-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="16342-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="16342-121">Notes</span><span class="sxs-lookup"><span data-stu-id="16342-121">Remarks</span></span>

<span data-ttu-id="16342-122">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="16342-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16342-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16342-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16342-124">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="16342-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="16342-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="16342-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="16342-126">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="16342-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="16342-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="16342-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="16342-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="16342-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="16342-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="16342-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="16342-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="16342-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="16342-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="16342-134">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="16342-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="16342-135">numberFormat</span><span class="sxs-lookup"><span data-stu-id="16342-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="16342-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="16342-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="16342-137">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="16342-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="16342-138">variables</span><span class="sxs-lookup"><span data-stu-id="16342-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="16342-139">enumRange</span><span class="sxs-lookup"><span data-stu-id="16342-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="16342-140">image</span><span class="sxs-lookup"><span data-stu-id="16342-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="16342-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="16342-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="16342-142">editControl</span><span class="sxs-lookup"><span data-stu-id="16342-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="16342-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="16342-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="16342-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="16342-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="16342-145">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="16342-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="16342-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="16342-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 

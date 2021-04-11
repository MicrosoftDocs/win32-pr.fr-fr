---
description: Un ID de modèle d’utilisateur d’application explicite (AppUserModelID) utilisé pour associer des processus, des fichiers et des fenêtres à une application particulière.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318889"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="a3382-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="a3382-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="a3382-104">Un ID de modèle d’utilisateur d’application explicite (AppUserModelID) utilisé pour associer des processus, des fichiers et des fenêtres à une application particulière.</span><span class="sxs-lookup"><span data-stu-id="a3382-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="a3382-105">Dans certains cas, il suffit de s’appuyer sur la AppUserModelID interne assignée à un processus par le système.</span><span class="sxs-lookup"><span data-stu-id="a3382-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="a3382-106">Toutefois, une application qui possède plusieurs processus ou une application en cours d’exécution dans un processus hôte peut avoir besoin de s’identifier de manière explicite par le biais de cette propriété afin de pouvoir regrouper ses fenêtres dans un même bouton de la barre des tâches et contrôler le contenu de la liste de raccourcis de cette application.</span><span class="sxs-lookup"><span data-stu-id="a3382-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="a3382-107">Pour définir cette propriété sur une fenêtre, utilisez [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et utilisez les méthodes de l’objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) récupéré pour définir la propriété [System.AppUserModel.ID]() de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3382-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="a3382-108">Pour plus d’informations, consultez [ID de modèle d’utilisateur d’application (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="a3382-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="a3382-109">Au moment de la définition de la propriété [System.AppUserModel.ID]() , la barre des tâches est notifiée pour actualiser ses informations dans la fenêtre ou le raccourci donné à ce AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="a3382-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="a3382-110">D’autres propriétés de fenêtre et de raccourci peuvent être utilisées conjointement avec une AppUserModelID explicite pour mieux contrôler le regroupement et l’épinglage associés à une fenêtre, le nom complet et l’icône utilisés dans la barre des tâches, ainsi que la commande de lancement d’une application épinglée à la barre des tâches ou d’une nouvelle instance de l’application via la liste de raccourcis de cette application.</span><span class="sxs-lookup"><span data-stu-id="a3382-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="a3382-111">Ces propriétés doivent être définies avant de définir la propriété [System.AppUserModel.ID]() .</span><span class="sxs-lookup"><span data-stu-id="a3382-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="a3382-112">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3382-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a3382-113">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="a3382-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="a3382-114">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="a3382-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="a3382-115">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="a3382-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="a3382-116">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="a3382-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a3382-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3382-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="a3382-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a3382-118">Remarks</span></span>

<span data-ttu-id="a3382-119">Les valeurs de la valeur de l’une sont définies dans propKey. h.</span><span class="sxs-lookup"><span data-stu-id="a3382-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3382-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3382-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3382-121">ID de modèle d’utilisateur d’application (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="a3382-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="a3382-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="a3382-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="a3382-123">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="a3382-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="a3382-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a3382-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a3382-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a3382-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a3382-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a3382-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a3382-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a3382-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a3382-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a3382-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a3382-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a3382-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a3382-135">variables</span><span class="sxs-lookup"><span data-stu-id="a3382-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="a3382-136">enumRange</span><span class="sxs-lookup"><span data-stu-id="a3382-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="a3382-137">image</span><span class="sxs-lookup"><span data-stu-id="a3382-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="a3382-138">drawControl</span><span class="sxs-lookup"><span data-stu-id="a3382-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a3382-139">editControl</span><span class="sxs-lookup"><span data-stu-id="a3382-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a3382-140">filterControl</span><span class="sxs-lookup"><span data-stu-id="a3382-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a3382-141">queryControl</span><span class="sxs-lookup"><span data-stu-id="a3382-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="a3382-142">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="a3382-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="a3382-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="a3382-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 

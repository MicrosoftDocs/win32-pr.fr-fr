---
title: Méthodes facultatives
description: Méthodes facultatives
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102381"
---
# <a name="optional-methods"></a><span data-ttu-id="5ffaa-103">Méthodes facultatives</span><span class="sxs-lookup"><span data-stu-id="5ffaa-103">Optional Methods</span></span>

<span data-ttu-id="5ffaa-104">Un composant OLE peut implémenter une interface sans implémenter toutes les sémantiques de chaque méthode de l’interface, à la place \_ NOTIMPL ou S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="5ffaa-105">Le tableau suivant décrit les méthodes qu’un conteneur de contrôles ActiveX n’est pas tenu d’implémenter (autrement dit, le conteneur de contrôle peut retourner E \_ NOTIMPL).</span><span class="sxs-lookup"><span data-stu-id="5ffaa-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="5ffaa-106">Le tableau ci-dessous décrit les méthodes facultatives. Notez que la méthode doit toujours exister, mais peut simplement retourner E \_ NOTIMPL au lieu d’implémenter la sémantique réelle.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="5ffaa-107">Notez que toute méthode d’une interface obligatoire qui n’est pas listée ci-dessous doit être considérée comme obligatoire et ne pas retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="5ffaa-108">Renvoyé</span><span class="sxs-lookup"><span data-stu-id="5ffaa-108">IOleClientSite</span></span>



| <span data-ttu-id="5ffaa-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-109">Method</span></span>                                                     | <span data-ttu-id="5ffaa-110">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ffaa-111">**SaveObject**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="5ffaa-112">Nécessaire pour que la persistance soit prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="5ffaa-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="5ffaa-114">Nécessaire uniquement si le conteneur prend en charge la liaison aux contrôles dans son propre formulaire ou document.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="5ffaa-115">IOleInPlaceSite</span><span class="sxs-lookup"><span data-stu-id="5ffaa-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="5ffaa-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-116">Method</span></span>                                                                     | <span data-ttu-id="5ffaa-117">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="5ffaa-118">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="5ffaa-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5ffaa-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="5ffaa-120">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="5ffaa-121">Peut retourner S \_ false sans action.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="5ffaa-122">**DiscardUndoState**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="5ffaa-123">Peut retourner S \_ OK sans action.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="5ffaa-124">**DeactivateAndUndo**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="5ffaa-125">La désactivation est obligatoire ; Undo est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="5ffaa-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="5ffaa-126">IOleControlSite</span></span>



| <span data-ttu-id="5ffaa-127">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-127">Method</span></span>                                                                          | <span data-ttu-id="5ffaa-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ffaa-129">**GetExtendedControl**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="5ffaa-130">Nécessaire pour les conteneurs qui prennent en charge les contrôles étendus.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="5ffaa-131">**ShowPropertyFrame**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="5ffaa-132">Nécessaire pour les conteneurs qui souhaitent inclure leurs propres pages de propriétés pour gérer les propriétés de contrôle étendues, en plus de celles fournies par un contrôle.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="5ffaa-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="5ffaa-134">Peut retourner S \_ false sans action.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="5ffaa-135">**LockInPlaceActive**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="5ffaa-136">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5ffaa-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="5ffaa-137">IDispatch (propriétés ambiantes)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="5ffaa-138">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-138">Method</span></span>                      | <span data-ttu-id="5ffaa-139">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5ffaa-140">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="5ffaa-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="5ffaa-141">Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="5ffaa-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5ffaa-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="5ffaa-143">Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="5ffaa-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="5ffaa-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="5ffaa-145">Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="5ffaa-146">IDispatch (récepteur d’événements)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="5ffaa-147">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-147">Method</span></span>                      | <span data-ttu-id="5ffaa-148">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffaa-149">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="5ffaa-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="5ffaa-150">Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="5ffaa-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5ffaa-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="5ffaa-152">Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="5ffaa-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="5ffaa-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="5ffaa-154">Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="5ffaa-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="5ffaa-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="5ffaa-156">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-156">Method</span></span>                                                                           | <span data-ttu-id="5ffaa-157">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="5ffaa-158">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="5ffaa-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="5ffaa-160">Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5ffaa-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="5ffaa-162">Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5ffaa-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="5ffaa-164">Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5ffaa-165">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="5ffaa-166">Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5ffaa-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="5ffaa-168">Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5ffaa-169">**RemoveMenus**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="5ffaa-170">Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)</span><span class="sxs-lookup"><span data-stu-id="5ffaa-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5ffaa-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="5ffaa-172">Nécessaire uniquement pour les conteneurs qui ont une ligne d’État</span><span class="sxs-lookup"><span data-stu-id="5ffaa-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="5ffaa-173">**EnableModeless**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="5ffaa-174">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5ffaa-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="5ffaa-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="5ffaa-176">Facultatif</span><span class="sxs-lookup"><span data-stu-id="5ffaa-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="5ffaa-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="5ffaa-177">IOleContainer</span></span>



| <span data-ttu-id="5ffaa-178">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ffaa-178">Method</span></span>                                                                    | <span data-ttu-id="5ffaa-179">Commentaires</span><span class="sxs-lookup"><span data-stu-id="5ffaa-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ffaa-180">**ParseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="5ffaa-181">Uniquement si la liaison aux contrôles ou à d’autres incorporations dans le conteneur est prise en charge, ce qui est nécessaire pour la liaison de moniker.</span><span class="sxs-lookup"><span data-stu-id="5ffaa-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="5ffaa-182">**LockContainer**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="5ffaa-183">Comme pour ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="5ffaa-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="5ffaa-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="5ffaa-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="5ffaa-185">Retourne tous les contrôles ActiveX via un énumérateur avec [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), mais pas nécessairement tous les objets (parce qu’il n’y a aucune garantie que tous les objets sont des contrôles ActiveX ; certains peuvent être des contrôles Windows normaux).</span><span class="sxs-lookup"><span data-stu-id="5ffaa-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5ffaa-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ffaa-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ffaa-187">Containers</span><span class="sxs-lookup"><span data-stu-id="5ffaa-187">Containers</span></span>](containers.md)
</dt> </dl>

 


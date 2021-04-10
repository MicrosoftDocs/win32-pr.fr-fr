---
title: Message WM_GETOBJECT (winuser. h)
description: Envoyé par Microsoft Active Accessibility et Microsoft UI Automation pour obtenir des informations sur un objet accessible contenu dans une application serveur.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT l’accessibilité des messages Windows
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106465"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="3ba2d-104">Message WM de \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="3ba2d-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="3ba2d-105">Envoyé par Microsoft Active Accessibility et Microsoft UI Automation pour obtenir des informations sur un objet accessible contenu dans une application serveur.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="3ba2d-106">Les applications n’envoient jamais ce message directement.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-106">Applications never send this message directly.</span></span> <span data-ttu-id="3ba2d-107">Microsoft Active Accessibility envoie ce message en réponse aux appels à [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="3ba2d-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="3ba2d-108">Toutefois, les applications serveur gèrent ce message.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-108">However, server applications handle this message.</span></span> <span data-ttu-id="3ba2d-109">UI Automation envoie ce message en réponse aux appels à [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)et [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), et lors de la gestion des événements pour lesquels un client s’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3ba2d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ba2d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba2d-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="3ba2d-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba2d-112">Fournit des informations supplémentaires sur le message et est utilisé uniquement par le système.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="3ba2d-113">Les serveurs transmettent *dwFlags* en tant que paramètre *wParam* dans l’appel à [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) lors du traitement du message.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="3ba2d-114">*dwObjId*</span><span class="sxs-lookup"><span data-stu-id="3ba2d-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba2d-115">Identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-115">Object identifier.</span></span> <span data-ttu-id="3ba2d-116">Cette valeur est l’une des constantes d' [identificateur d’objet](object-identifiers.md) ou un identificateur d’objet personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="3ba2d-117">Une application serveur doit vérifier cette valeur pour identifier le type d’informations demandées.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="3ba2d-118">Avant de comparer cette valeur aux \_ valeurs objid, le serveur doit le caster en **DWORD**. dans le cas contraire, sur Windows 64 bits, l’extension de signe du *lParam* peut interférer avec la comparaison.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="3ba2d-119">Si *dwObjId* est l’une des \_ valeurs objid telles que [**objID \_ client**](object-identifiers.md), la demande concerne un objet Microsoft Active Accessibility qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="3ba2d-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="3ba2d-120">Si *dwObjId* est égal à **UiaRootObjectId**, la demande est pour un fournisseur UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="3ba2d-121">Si le serveur implémente UI Automation, il doit retourner un fournisseur à l’aide de la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="3ba2d-122">Si *dwObjId* est [**objID \_ NATIVEOM**](object-identifiers.md), la demande est pour le modèle objet sous-jacent du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="3ba2d-123">Si le contrôle prend en charge cette requête, il doit retourner une interface COM appropriée en appelant la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="3ba2d-124">Si *dwObjId* est [**objID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la demande est que le contrôle s’identifie comme un contrôle Windows standard ou un contrôle commun implémenté par la bibliothèque de contrôles communs (ComCtrl.dll).</span><span class="sxs-lookup"><span data-stu-id="3ba2d-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba2d-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ba2d-125">Return value</span></span>

<span data-ttu-id="3ba2d-126">Si la fenêtre ou le contrôle n’a pas besoin de répondre à ce message, elle doit passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; Sinon, la fenêtre ou le contrôle doit retourner une valeur qui correspond à la demande spécifiée par *dwObjId*:</span><span class="sxs-lookup"><span data-stu-id="3ba2d-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="3ba2d-127">Si la fenêtre ou le contrôle implémente l’Automation d’interface utilisateur, la fenêtre ou le contrôle doit retourner la valeur obtenue par un appel à la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="3ba2d-128">Si *dwObjId* est [**objID \_ NATIVEOM**](object-identifiers.md) et que la fenêtre expose un modèle objet natif, les fenêtres doivent retourner la valeur obtenue par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="3ba2d-129">Si *dwObjId* est [**un \_ client objid**](object-identifiers.md) et que la fenêtre implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la fenêtre doit retourner la valeur obtenue par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba2d-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3ba2d-130">Remarks</span></span>

<span data-ttu-id="3ba2d-131">Lorsqu’un client appelle [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou l’une des autres fonctions **AccessibleObjectFrom**_X_ qui récupèrent une interface vers un objet, Microsoft Active Accessibility envoie le message **WM \_ GETOBJECT** à la procédure de fenêtre appropriée au sein de l’application serveur appropriée.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="3ba2d-132">Lors du traitement de **WM \_ GETOBJECT**, les applications serveur appellent [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) et utilisent la valeur de retour de cette fonction comme valeur de retour pour le message.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="3ba2d-133">Microsoft Active Accessibility, conjointement avec la bibliothèque COM, effectue le marshaling approprié et transmet le pointeur d’interface du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="3ba2d-134">Les serveurs ne répondent pas à l’objet **WM \_ GETOBJECT** avant l’initialisation complète de l’objet ou après le début de la fermeture.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="3ba2d-135">Quand une application crée une nouvelle fenêtre, le système envoie [**l' \_ objet d’événement \_ Create**](event-constants.md) pour notifier les clients avant d’envoyer le message [WM \_ Create](../winmsg/wm-create.md) à la procédure de fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="3ba2d-136">Étant donné que de nombreuses applications utilisent \_ la création de WM pour démarrer leur processus d’initialisation, les serveurs ne répondent pas au message **WM WM \_** avant la fin du traitement du message **WM \_ Create** .</span><span class="sxs-lookup"><span data-stu-id="3ba2d-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="3ba2d-137">Un serveur utilise le **WM \_ GETOBJECT** pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ba2d-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="3ba2d-138">Créer des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="3ba2d-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="3ba2d-139">Réutiliser des pointeurs existants vers des objets</span><span class="sxs-lookup"><span data-stu-id="3ba2d-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="3ba2d-140">Créer des interfaces vers le même objet</span><span class="sxs-lookup"><span data-stu-id="3ba2d-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="3ba2d-141">Pour les clients, cela signifie qu’ils peuvent recevoir des pointeurs d’interface distincts pour le même élément d’interface utilisateur, en fonction de l’action du serveur.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="3ba2d-142">Pour déterminer si deux pointeurs d’interface pointent vers le même élément d’interface utilisateur, les clients comparent les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="3ba2d-143">La comparaison des pointeurs ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="3ba2d-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba2d-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ba2d-144">Requirements</span></span>



| <span data-ttu-id="3ba2d-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ba2d-145">Requirement</span></span> | <span data-ttu-id="3ba2d-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ba2d-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba2d-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ba2d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba2d-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ba2d-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ba2d-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ba2d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba2d-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ba2d-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ba2d-151">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3ba2d-151">Redistributable</span></span><br/>          | <span data-ttu-id="3ba2d-152">Active Accessibility 1,3 RDK sur Windows NT 4,0 avec SP6 et versions ultérieures et Windows 95</span><span class="sxs-lookup"><span data-stu-id="3ba2d-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="3ba2d-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ba2d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba2d-154"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ba2d-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba2d-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ba2d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba2d-156">Comment gérer WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="3ba2d-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="3ba2d-157">Fonctionnement de la fonction GETOBJECT de WM \_</span><span class="sxs-lookup"><span data-stu-id="3ba2d-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="3ba2d-158">**LresultFromObject**</span><span class="sxs-lookup"><span data-stu-id="3ba2d-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 


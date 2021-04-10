---
title: Comment exposer un fournisseur UI Automation Server-Side
description: Cette rubrique contient un exemple de code qui montre comment exposer un fournisseur UI Automation côté serveur pour un contrôle personnalisé.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196984"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="7b64d-103">Comment exposer un fournisseur UI Automation Server-Side</span><span class="sxs-lookup"><span data-stu-id="7b64d-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="7b64d-104">Cette rubrique contient un exemple de code qui montre comment exposer un fournisseur UI Automation côté serveur pour un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7b64d-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="7b64d-105">L’Automation d’interface utilisateur Microsoft envoie le message [**WM \_ GETOBJECT**](wm-getobject.md) à une application fournisseur pour récupérer des informations sur un objet accessible pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7b64d-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="7b64d-106">UI Automation envoie **WM \_ GETOBJECT** lorsqu’un client appelle [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)et [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), et lors de la gestion des événements pour lesquels le client s’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="7b64d-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="7b64d-107">Lorsqu’un fournisseur reçoit un message [**WM \_ GETOBJECT**](wm-getobject.md) , il doit vérifier si le paramètre *lParam* est égal à **UiaRootObjectId**.</span><span class="sxs-lookup"><span data-stu-id="7b64d-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="7b64d-108">Si c’est le cas, le fournisseur doit retourner l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b64d-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="7b64d-109">Le fournisseur retourne l’interface en appelant la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="7b64d-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="7b64d-110">L’exemple suivant montre comment répondre à [**WM \_ GETOBJECT**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="7b64d-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a><span data-ttu-id="7b64d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b64d-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7b64d-112">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="7b64d-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7b64d-113">Implémentation d’un fournisseur UI Automation Server-Side</span><span class="sxs-lookup"><span data-stu-id="7b64d-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="7b64d-114">Le message WM de \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="7b64d-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="7b64d-115">Rubriques de procédures pour les fournisseurs UI Automation</span><span class="sxs-lookup"><span data-stu-id="7b64d-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 





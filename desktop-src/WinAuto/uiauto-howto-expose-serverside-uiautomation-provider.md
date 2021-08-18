---
title: Comment exposer un fournisseur UI Automation Server-Side
description: Cette rubrique contient un exemple de code qui montre comment exposer un fournisseur UI Automation côté serveur pour un contrôle personnalisé.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133312"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Comment exposer un fournisseur UI Automation Server-Side

Cette rubrique contient un exemple de code qui montre comment exposer un fournisseur UI Automation côté serveur pour un contrôle personnalisé.

L’Automation d’interface utilisateur Microsoft envoie le message [**WM \_ GETOBJECT**](wm-getobject.md) à une application fournisseur pour récupérer des informations sur un objet accessible pris en charge par le fournisseur. UI Automation envoie **WM \_ GETOBJECT** lorsqu’un client appelle [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)et [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), et lors de la gestion des événements pour lesquels le client s’est inscrit.

Lorsqu’un fournisseur reçoit un message [**WM \_ GETOBJECT**](wm-getobject.md) , il doit vérifier si le paramètre *lParam* est égal à **UiaRootObjectId**. Si c’est le cas, le fournisseur doit retourner l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) de l’objet. Le fournisseur retourne l’interface en appelant la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .

L’exemple suivant montre comment répondre à [**WM \_ GETOBJECT**](wm-getobject.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation d’un fournisseur UI Automation Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Le message WM de \_ GETOBJECT](the-wm-getobject-message.md)
</dt> <dt>

[Rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 





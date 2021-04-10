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
# <a name="wm_getobject-message"></a>Message WM de \_ GETOBJECT

Envoyé par Microsoft Active Accessibility et Microsoft UI Automation pour obtenir des informations sur un objet accessible contenu dans une application serveur.

Les applications n’envoient jamais ce message directement. Microsoft Active Accessibility envoie ce message en réponse aux appels à [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). Toutefois, les applications serveur gèrent ce message. UI Automation envoie ce message en réponse aux appels à [**IUIAutomation :: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)et [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), et lors de la gestion des événements pour lesquels un client s’est inscrit.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* 
</dt> <dd>

Fournit des informations supplémentaires sur le message et est utilisé uniquement par le système. Les serveurs transmettent *dwFlags* en tant que paramètre *wParam* dans l’appel à [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) lors du traitement du message.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificateur d’objet. Cette valeur est l’une des constantes d' [identificateur d’objet](object-identifiers.md) ou un identificateur d’objet personnalisé. Une application serveur doit vérifier cette valeur pour identifier le type d’informations demandées. Avant de comparer cette valeur aux \_ valeurs objid, le serveur doit le caster en **DWORD**. dans le cas contraire, sur Windows 64 bits, l’extension de signe du *lParam* peut interférer avec la comparaison.

-   Si *dwObjId* est l’une des \_ valeurs objid telles que [**objID \_ client**](object-identifiers.md), la demande concerne un objet Microsoft Active Accessibility qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Si *dwObjId* est égal à **UiaRootObjectId**, la demande est pour un fournisseur UI Automation. Si le serveur implémente UI Automation, il doit retourner un fournisseur à l’aide de la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si *dwObjId* est [**objID \_ NATIVEOM**](object-identifiers.md), la demande est pour le modèle objet sous-jacent du contrôle. Si le contrôle prend en charge cette requête, il doit retourner une interface COM appropriée en appelant la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si *dwObjId* est [**objID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), la demande est que le contrôle s’identifie comme un contrôle Windows standard ou un contrôle commun implémenté par la bibliothèque de contrôles communs (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fenêtre ou le contrôle n’a pas besoin de répondre à ce message, elle doit passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; Sinon, la fenêtre ou le contrôle doit retourner une valeur qui correspond à la demande spécifiée par *dwObjId*:

-   Si la fenêtre ou le contrôle implémente l’Automation d’interface utilisateur, la fenêtre ou le contrôle doit retourner la valeur obtenue par un appel à la fonction [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Si *dwObjId* est [**objID \_ NATIVEOM**](object-identifiers.md) et que la fenêtre expose un modèle objet natif, les fenêtres doivent retourner la valeur obtenue par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Si *dwObjId* est [**un \_ client objid**](object-identifiers.md) et que la fenêtre implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la fenêtre doit retourner la valeur obtenue par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

## <a name="remarks"></a>Notes

Lorsqu’un client appelle [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou l’une des autres fonctions **AccessibleObjectFrom**_X_ qui récupèrent une interface vers un objet, Microsoft Active Accessibility envoie le message **WM \_ GETOBJECT** à la procédure de fenêtre appropriée au sein de l’application serveur appropriée. Lors du traitement de **WM \_ GETOBJECT**, les applications serveur appellent [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) et utilisent la valeur de retour de cette fonction comme valeur de retour pour le message. Microsoft Active Accessibility, conjointement avec la bibliothèque COM, effectue le marshaling approprié et transmet le pointeur d’interface du serveur au client.

Les serveurs ne répondent pas à l’objet **WM \_ GETOBJECT** avant l’initialisation complète de l’objet ou après le début de la fermeture. Quand une application crée une nouvelle fenêtre, le système envoie [**l' \_ objet d’événement \_ Create**](event-constants.md) pour notifier les clients avant d’envoyer le message [WM \_ Create](../winmsg/wm-create.md) à la procédure de fenêtre de l’application. Étant donné que de nombreuses applications utilisent \_ la création de WM pour démarrer leur processus d’initialisation, les serveurs ne répondent pas au message **WM WM \_** avant la fin du traitement du message **WM \_ Create** .

Un serveur utilise le **WM \_ GETOBJECT** pour effectuer les tâches suivantes :

-   [Créer des objets accessibles](create-new-accessible-objects.md)
-   [Réutiliser des pointeurs existants vers des objets](reuse-existing-pointers-to-objects.md)
-   [Créer des interfaces vers le même objet](create-new-interfaces-to-the-same-object.md)

Pour les clients, cela signifie qu’ils peuvent recevoir des pointeurs d’interface distincts pour le même élément d’interface utilisateur, en fonction de l’action du serveur. Pour déterminer si deux pointeurs d’interface pointent vers le même élément d’interface utilisateur, les clients comparent les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet. La comparaison des pointeurs ne fonctionne pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| Composant redistribuable<br/>          | Active Accessibility 1,3 RDK sur Windows NT 4,0 avec SP6 et versions ultérieures et Windows 95<br/>              |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Comment gérer WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[Fonctionnement de la fonction GETOBJECT de WM \_](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 


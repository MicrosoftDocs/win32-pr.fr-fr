---
title: Récupération d’un objet IAccessible
description: Microsoft Active Accessibility fournit des fonctions telles que AccessibleObjectFromWindow et AccessibleObjectFromPoint qui permettent aux clients de récupérer des objets accessibles.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010651"
---
# <a name="retrieving-an-iaccessible-object"></a>Récupération d’un objet IAccessible

Microsoft Active Accessibility fournit des fonctions telles que [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) qui permettent aux clients de récupérer des objets accessibles. Ces fonctions retournent un pointeur d’interface [**IDispatch**](idispatch-interface.md) ou [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) par le biais duquel les clients obtiennent des informations sur l’objet accessible.

Lorsqu’un client appelle [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou l’une des autres fonctions **AccessibleObjectFrom**_X_ qui récupèrent une interface vers un objet, Microsoft Active Accessibility envoie le message de fenêtre [**WM \_ GETOBJECT**](wm-getobject.md) à la procédure de fenêtre applicable au sein de l’application appropriée. Pour fournir des informations aux clients, les serveurs doivent répondre au message **WM de \_ GETOBJECT** .

Pour collecter des informations spécifiques sur un élément d’interface utilisateur, les clients doivent d’abord récupérer une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément. Pour récupérer un objet **IAccessible** d’un élément, les clients peuvent utiliser l’une des fonctions suivantes :

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Pour récupérer un pointeur d’interface IAccessible**

1.  Le client appelle l’une des fonctions **AccessibleObjectFrom**_X_ .
2.  Oleacc.dll envoie un message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) au serveur.
3.  Le serveur détermine l’élément d’interface utilisateur qui correspond à la demande.
4.  Le serveur retourne la valeur zéro pour demander un proxy Oleacc.dll,

    ou

    Retourne un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implémentation native). Pour ce faire, procédez comme suit :

    -   Construit un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour l’élément.
    -   Appelle [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) pour marshaler le pointeur de l’objet.
    -   Retourne la LRESULT à Oleacc.dll.

5.  Oleacc.dll examine la valeur renvoyée par [**WM \_ GETOBJECT**](wm-getobject.md).

    Si la valeur est égale à zéro, Oleacc.dll construit un objet proxy et le retourne au client.

    ou

    Si la valeur est différente de zéro, Oleacc.dll appelle [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) pour démarshaler le pointeur d’objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) natif et le retourne au client.

 

 





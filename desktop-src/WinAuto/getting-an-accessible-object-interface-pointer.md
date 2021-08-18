---
title: Obtention d’un pointeur d’interface d’objet accessible
description: Les applications clientes Microsoft Active Accessibility récupèrent les pointeurs d’interface aux objets accessibles à l’aide de l’une des fonctions suivantes.
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ea0d7936671a68c140c6d22fdc3afdad0db0899c9c2cbc51637dcf36d9ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994199"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>Obtention d’un pointeur d’interface d’objet accessible

Les applications clientes Microsoft Active Accessibility récupèrent les pointeurs d’interface aux objets accessibles à l’aide de l’une des fonctions suivantes.

**AccessibleObjectFromEvent**

De nombreux clients recherchent des informations sur des objets accessibles spécifiques qui génèrent des événements. Étant donné que l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est la « passerelle » aux objets accessibles, les clients doivent disposer d’un moyen simple d’associer [winEvents](winevents-overview.md) à l’interface **IAccessible** de l’objet qui génère les événements. Microsoft Active Accessibility fournit la fonction [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) spécifiquement à cet effet.

> [!Note]  
> Les clients avec des [fonctions de raccordement dans le contexte](in-context-hook-functions.md) doivent appeler la fonction [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow) avant d’appeler [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

La fonction [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) accepte une grande partie des mêmes informations que celles reçues par la [*fonction de raccordement*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) d’un client. Quand une fonction de raccordement client reçoit une notification d’événement, elle passe les paramètres appropriés des événements à **AccessibleObjectFromEvent**.

La fonction récupère l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’élément d’interface utilisateur qui a généré l’événement ou l’interface de l’objet parent de l’élément. Si le pointeur d’interface de l’objet parent est retourné, le client appelle les propriétés et les méthodes du parent pour obtenir des informations sur l’élément enfant qui a généré l’événement.

**AccessibleObjectFromPoint**

Pour récupérer l’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’un objet à un point spécifié sur l’écran, les clients utilisent la fonction [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) .

**AccessibleObjectFromWindow**

Pour récupérer l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’un objet à partir d’un handle de fenêtre, les clients utilisent la fonction [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

Il est possible que les serveurs retournent des pointeurs d’interface distincts pour le même élément d’interface utilisateur chaque fois que la fonction [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) est appelée. Pour déterminer si deux pointeurs font référence au même élément d’interface utilisateur, les développeurs clients doivent comparer les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de l’objet, et non les pointeurs.

 

 
---
title: Fonctionnement de WM_GETOBJECT
description: Microsoft Active Accessibility envoie le \_ message WM GETOBJECT à l’application serveur appropriée lorsqu’un client appelle l’une des fonctions AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795759"
---
# <a name="how-wm_getobject-works"></a>Fonctionnement de la fonction GETOBJECT de WM \_

Microsoft Active Accessibility envoie le message [**WM \_ GETOBJECT**](wm-getobject.md) à l’application serveur appropriée lorsqu’un client appelle l’une des fonctions **AccessibleObjectFrom**_X_ . La liste suivante décrit les différents scénarios qui se produisent :

-   Si la fenêtre ou le contrôle qui reçoit le [**WM \_ GETOBJECT**](wm-getobject.md) implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la fenêtre retourne une référence à l’interface **IAccessible** à l’aide de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, conjointement avec la bibliothèque COM (Component Object Model), effectue le marshaling approprié et transmet le pointeur d’interface du serveur au client.
-   Si la fenêtre qui reçoit le message n’implémente pas [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), elle doit retourner zéro.
-   Si la fenêtre ne gère pas le message [**WM \_ GETOBJECT**](wm-getobject.md) , la fonction [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retourne la valeur zéro.

Même si le serveur retourne la valeur zéro, Microsoft Active Accessibility fournit toujours au client des informations sur l’objet. Pour la plupart des objets fournis par le système, tels que les zones de liste et les boutons, Microsoft Active Accessibility fournit des informations complètes. pour les autres objets, les informations sont limitées. Par exemple, Microsoft Active Accessibility ne fournit pas d’informations pour les contrôles qui n’ont pas de handle de fenêtre. Microsoft Active Accessibility retourne un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en proxy utilisé par le client pour obtenir des informations sur l’objet.

Pour plus d’informations, consultez [le \_ message WM GETOBJECT](the-wm-getobject-message.md).

 

 
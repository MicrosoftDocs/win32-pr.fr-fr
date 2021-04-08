---
title: Comment gérer les WM_GETOBJECT
description: Lorsqu’il reçoit un message WM de \_ la fonction GETOBJECT qui contient \_ le client objid, le serveur doit retourner un pointeur vers l’objet qui implémente IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674010"
---
# <a name="how-to-handle-wm_getobject"></a>Comment gérer WM \_ GETOBJECT

Lorsqu’il reçoit un message WM de la fonction [**\_ GETOBJECT**](wm-getobject.md) qui contient le [**\_ client objid**](object-identifiers.md), le serveur doit retourner un pointeur vers l’objet qui implémente [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Ce pointeur est un LRESULT obtenu en appelant [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, conjointement avec la bibliothèque COM (Component Object Model), effectue le marshaling approprié et passe le pointeur d’interface **IAccessible** du serveur au client.

Les serveurs doivent gérer correctement le décompte de références sur l’objet accessible. N’oubliez pas que lorsque vous créez un objet COM, le nombre de références est 1. [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) incrémente ensuite le nombre de références plusieurs fois. Toutes les références créées par **LresultFromObject** sont automatiquement libérées quand l’objet n’est plus nécessaire, mais que le serveur est responsable de la libération de la référence initiale et, à moins qu’elle le fasse, l’objet ne sera jamais détruit. Les exemples des sections suivantes montrent comment libérer des références aux objets accessibles.

En général, les serveurs gèrent [**WM \_ GETOBJECT**](wm-getobject.md) de l’une des manières suivantes :

-   [Créer des objets accessibles](create-new-accessible-objects.md)
-   [Réutiliser des pointeurs existants vers des objets](reuse-existing-pointers-to-objects.md)
-   [Créer des interfaces vers le même objet](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> Dans cette section, comme dans le reste de la documentation, lorsqu’un pointeur vers une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est abordé, ce pointeur peut en fait être un pointeur vers un objet proxy qui encapsule l’interface **IAccessible** . Pour plus d’informations sur les objets proxy, consultez [création d’objets proxy](creating-proxy-objects.md).

 

Pour obtenir une vue d’ensemble de [**WM \_ GetObject**](wm-getobject.md), consultez fonctionnement de [WM \_ GetObject](how-wm-getobject-works.md).

 

 





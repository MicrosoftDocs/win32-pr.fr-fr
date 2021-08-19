---
title: Présentation des objets proxy
description: Un objet proxy joue le rôle d’intermédiaire entre le client et un objet accessible. L’objectif de l’objet proxy est de surveiller l’étendue de la durée de vie de l’objet accessible et de transférer les appels à l’objet accessible uniquement s’il n’est pas détruit.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf3625bf048241e4ef28163ed3b8ca7916ccc35cccc12e7eac05b2b9b9c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052187"
---
# <a name="what-are-proxy-objects"></a>Que sont les objets proxy ?

Un objet *proxy* joue le rôle d’intermédiaire entre le client et un objet accessible. L’objectif de l’objet proxy est de surveiller l’étendue de la durée de vie de l’objet accessible et de transférer les appels à l’objet accessible uniquement s’il n’est pas détruit.

Lorsqu’un client appelle une propriété [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour obtenir des informations sur un objet, l’objet proxy doit vérifier si l’objet accessible est toujours disponible. Si c’est le cas, l’objet proxy transmet la requête du client à l’objet accessible. Si l’objet accessible est détruit (par exemple, lorsqu’une boîte de dialogue avec des contrôles personnalisés est fermée), l’objet proxy retourne une erreur. Pour indiquer que l’objet a été détruit, il est recommandé que les serveurs retournent le code d’erreur **co \_ E \_ OBJNOTCONNECTED** , car cette erreur est retournée par le modèle COM (Component Object Model) après qu’un serveur a appelé [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).

L’objet proxy est transparent pour le client. Lorsque le client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), il reçoit un pointeur vers une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Toutefois, lorsque le client utilise ce pointeur pour appeler l’une des propriétés ou méthodes **IAccessible** , le code exécuté se trouve dans l’objet proxy.

 

 
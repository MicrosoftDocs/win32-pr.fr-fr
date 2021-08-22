---
title: Délégation de QueryInterface
description: Délégation de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501209"
---
# <a name="delegation-of-queryinterface"></a>Délégation de QueryInterface

Les gestionnaires qui requièrent l’accès à certaines des interfaces internes du gestionnaire proxy doivent parcourir l’interface [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) . Cela empêche les gestionnaires de déléguer et d’exposer aveuglément les interfaces internes de l’agrégat en dehors de l’agrégat. Ces interfaces incluent [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) et [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Si le gestionnaire souhaite exposer **IClientSecurity** ou **IMultiQI**, il doit les implémenter lui-même.

Dans le cas de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), si le client tente de définir la sécurité sur une interface exposée par le gestionnaire, le gestionnaire doit définir la sécurité sur le proxy d’interface réseau sous-jacent.

Dans le cas de [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), le gestionnaire doit remplir les interfaces qu’il connaît, puis transférer l’appel au gestionnaire de proxy pour que le reste des interfaces soit rempli.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de Client-Side léger](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 
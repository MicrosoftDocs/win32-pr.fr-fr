---
title: Initialisation d’objets persistants
description: Initialisation d’objets persistants
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363643"
---
# <a name="initializing-persistent-objects"></a>Initialisation d’objets persistants

Plusieurs interfaces d’objets persistants, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))et [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), permettent aux clients d’initialiser des objets à un état « actualisé » ou « par défaut ». Cet état initial est différent de celui d’un objet nouvellement créé, qui n’a pas d’État.

L’initialisation de l’état d’un objet, même à l’État par défaut, peut être une opération gourmande en ressources ou nécessitant beaucoup de ressources. En séparant la création de l’initialisation, l’initialisation ne peut être effectuée que lorsqu’elle est réellement nécessaire et que les clients peuvent éviter d’initialiser les objets à l’État par défaut pour charger immédiatement les données précédemment stockées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’objets persistants](persistent-object-interfaces.md)
</dt> </dl>

 

 
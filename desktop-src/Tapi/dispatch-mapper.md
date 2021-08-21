---
description: Le mappeur de répartition est créé à l’aide de COM CoCreateInstance et expose une interface, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Mappeur de répartition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0880228ab608abe5f599d58bb47d211d1458dd49636a9bdc992f31dfa26c028
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866683"
---
# <a name="dispatch-mapper"></a>Mappeur de répartition

Le mappeur de répartition est créé à l’aide de COM **CoCreateInstance** et expose une interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper). Cette interface permet à une application de récupérer le pointeur de dispatch d’une autre interface sur un objet, en fonction du pointeur de dispatch d’une interface et du GUID d’un autre. Cette interface est fournie pour aider les programmeurs à utiliser des applications de script qui ne fournissent pas de moyen d’interroger facilement les interfaces sur un objet.

Le mappeur de dispatch utilise l’interface **IObjectSafety** d’un objet pour s’assurer que l’objet est sécurisé pour l’écriture de scripts sur l’interface demandée. Si l’objet n’implémente pas **IObjectSafety**, ou si l’objet n’est pas sécurisé sur cette interface particulière, l’appel échoue.

 

 




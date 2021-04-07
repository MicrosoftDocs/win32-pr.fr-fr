---
title: Ordre de causalité des appels asynchrones
description: Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029131"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Ordre de causalité des appels asynchrones

Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle. La bibliothèque Runtime RPC gère cette situation comme suit :

-   Le mécanisme RPC asynchrone garantit que les appels asynchrones effectués sur le même handle de liaison, sur le même thread, au même niveau de sécurité, sont distribués dans l’ordre dans lequel ils ont été créés. L’exécution réelle des appels peut se produire dans le désordre.
-   Comme pour les appels synchrones, les appels de procédure distante asynchrones de différents threads clients s’exécutent simultanément.
-   Si un appel asynchrone à partir d’une application cliente est suivi d’un ou de plusieurs appels synchrones, l’appel asynchrone peut s’exécuter pendant l’exécution des appels synchrones. Quel que soit l’état de l’appel asynchrone, les appels synchrones sont exécutés dans l’ordre dans lequel ils sont reçus par le serveur.
-   Si une application cliente sélectionne le classement non causalité pour un handle de liaison particulier, elle désactive la sérialisation pour ce handle. Les applications activent le classement sans causalité en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) avec le paramètre *option* défini sur \_ liaison RPC C opt not \_ \_ \_ causalité et le paramètre *OptionValue* défini sur **true**. Pour plus d’informations, consultez [constantes d’option de liaison](binding-option-constants.md).

 

 





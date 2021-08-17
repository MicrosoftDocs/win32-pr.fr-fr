---
title: Ordre de causalité des appels asynchrones
description: Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbafc5f9166d28a80d514abd4ebea20ab01ea32f542561e2108feae4a5769458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932293"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Ordre de causalité des appels asynchrones

Dans une application RPC asynchrone, il est possible pour un thread client d’effectuer un deuxième appel asynchrone sur un handle de liaison avant la fin d’un appel antérieur effectué sur ce handle. La bibliothèque Runtime RPC gère cette situation comme suit :

-   Le mécanisme RPC asynchrone garantit que les appels asynchrones effectués sur le même handle de liaison, sur le même thread, au même niveau de sécurité, sont distribués dans l’ordre dans lequel ils ont été créés. L’exécution réelle des appels peut se produire dans le désordre.
-   Comme pour les appels synchrones, les appels de procédure distante asynchrones de différents threads clients s’exécutent simultanément.
-   Si un appel asynchrone à partir d’une application cliente est suivi d’un ou de plusieurs appels synchrones, l’appel asynchrone peut s’exécuter pendant l’exécution des appels synchrones. Quel que soit l’état de l’appel asynchrone, les appels synchrones sont exécutés dans l’ordre dans lequel ils sont reçus par le serveur.
-   Si une application cliente sélectionne le classement non causalité pour un handle de liaison particulier, elle désactive la sérialisation pour ce handle. Les applications activent le classement sans causalité en appelant [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) avec le paramètre *option* défini sur \_ liaison RPC C opt not \_ \_ \_ causalité et le paramètre *OptionValue* défini sur **true**. Pour plus d’informations, consultez [constantes d’option de liaison](binding-option-constants.md).

 

 





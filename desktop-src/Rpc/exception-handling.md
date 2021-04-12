---
title: Gestion des exceptions (RPC)
description: RPC utilise la même approche pour la gestion des exceptions que l’API Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25de594a648cddb70f26b42e8b0dbf1d6a9dd51d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464131"
---
# <a name="exception-handling-rpc"></a>Gestion des exceptions (RPC)

RPC utilise la même approche pour la gestion des exceptions que l’API Windows.

La structure [**RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) est équivalente à l’instruction Windows **try-finally** . La construction d’exception RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) est équivalente à l’instruction **try-except** Windows.

Lorsque vous utilisez les gestionnaires d’exceptions RPC, le code source côté client est portable. Les différents fichiers d’en-tête RPC fournis pour chaque plateforme résolvent les macros **RpcTry** et [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) pour chaque plateforme. Dans l’environnement Windows, ces macros sont mappées directement aux instructions **try-finally** et **try-except** de Windows. Dans d’autres environnements, ces macros sont mappées à d’autres implémentations spécifiques à la plateforme de gestionnaires d’exceptions.

Les exceptions potentielles générées par ces structures incluent l’ensemble des codes d’erreur retournés par les fonctions RPC avec les préfixes RPC \_ S \_ et RPC \_ X et l’ensemble des exceptions retournées par Windows. Pour plus d’informations, consultez [valeurs de retour RPC](rpc-return-values.md).

Tandis que les macros **RpcTry** et [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) offrent une méthode personnalisable et indépendante de la plateforme pour gérer les exceptions, dans Windows Vista et les versions ultérieures de Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) est la méthode recommandée pour gérer les exceptions. Il n’est pas nécessaire d’écrire des filtres personnalisés pour capturer la plupart des exceptions structurées les plus courantes. Toutefois, les filtres d’exceptions personnalisés requièrent toujours **RpcExcept**.

Les exceptions qui se produisent dans l’application serveur, le stub serveur et la bibliothèque Runtime de serveur (au-dessus de la couche de transport) sont propagées au client. Aucune exception n’est propagée à partir du niveau de transport serveur. La méthode recommandée pour qu’une routine de serveur retourne des erreurs au moment de l’exécution RPC consiste à lever une exception. Une routine de serveur peut utiliser toutes les méthodes appropriées pour la communication des erreurs entre les routines du serveur, mais si elle rencontre une erreur qui l’empêche d’exécuter la procédure distante, elle doit lever une exception après le nettoyage et le retour à l’heure d’exécution RPC, au lieu de retourner une valeur RPC que seule la routine du serveur reconnaît comme une erreur.

L’illustration suivante montre comment les exceptions sont retournées du serveur au client.

![les exceptions sont retournées du serveur au client par le biais de l’exécution RPC respective de chaque composant](images/prog-a20.png)

Les gestionnaires d’exceptions RPC diffèrent légèrement des macros de gestion des exceptions (OSF-DCE) Open Software Foundation-Distributed Computing Environment (OSF-ETCD) **try**, **finally** et **catch**. Différents fournisseurs proposent des fichiers include qui mappent les fonctions RPC OSF-DCE aux fonctions RPC de Microsoft, notamment **try**, **catch**, **catch** \_ **All** et **EndTry**. Ces fichiers d’en-tête mappent également les \_ \_ \* codes d’erreur s RPC sur les équivalents d’exception OSF-DCE, RPC \_ S \_ \* et mappent les \_ \_ \* codes d’erreur RPC x à RPC \_ x \_ \* . Pour la portabilité de l’OSF-DCE, utilisez ces fichiers include. Pour plus d’informations sur les gestionnaires d’exceptions RPC, consultez [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Pour plus d’informations sur les gestionnaires d’exceptions Windows, consultez [gestion structurée des exceptions](/windows/desktop/Debug/structured-exception-handling).

 

 

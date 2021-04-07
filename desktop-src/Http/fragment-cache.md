---
title: Cache de fragments
description: L’API du serveur HTTP fournit des fonctionnalités permettant aux utilisateurs de stocker des fragments de données dans un cache pour les utiliser dans la formation rapide des réponses HTTP.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3979fb03c4f8898644329fd27eafb7007adbcc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939752"
---
# <a name="fragment-cache"></a>Cache de fragments

L’API du serveur HTTP fournit des fonctionnalités permettant aux utilisateurs de stocker des fragments de données dans un cache pour les utiliser dans la formation rapide des réponses HTTP.

Les fragments peuvent être ajoutés au cache en appelant la fonction [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) . Un fragment est identifié par une URL contenue dans le paramètre *pUrlPrefix* . Un appel à cette fonction avec l’URL d’un fragment existant remplace le fragment existant.

Un fragment peut être supprimé ou remplacé par le propriétaire de la file d’attente de demandes qui a ajouté le fragment pour la première fois. La fonction [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) appelée avec un URLPrefix supprime tous les fragments de ce préfixe, ainsi que les descendants hiérarchiques de ce URLPrefix. La fonction [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) lit le fragment entier ou une plage d’octets spécifiée dans le fragment.

> [!Note]  
> L’ajout d’un fragment au cache ne garantit pas qu’il est disponible pour les appels ultérieurs pour envoyer une réponse. Les entrées du cache de fragments peuvent devenir indisponibles à tout moment. Un appel qui utilise un fragment qui n’est pas disponible échoue. Les applications qui utilisent le cache de fragments doivent être préparées pour gérer cet échec.

 

## <a name="sending-a-response-with-a-fragment"></a>Envoi d’une réponse avec un fragment

Les fragments peuvent être utilisés pour former la totalité ou une partie d’un corps d’entité de réponse HTTP. Vous pouvez envoyer une réponse et un corps d’entité dans un appel à la fonction [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) en spécifiant un tableau de structures de [**\_ \_ blocs de données http**](/windows/desktop/api/Http/ns-http-http_data_chunk) dans la structure de [**\_ réponse http**](http-response.md) .

Un [**\_ \_ segment de données http**](/windows/desktop/api/Http/ns-http-http_data_chunk) peut spécifier un bloc de mémoire, un descripteur d’un fichier déjà ouvert ou une entrée de cache de fragments. Celles-ci correspondent aux types de **\_ \_ blocs de données http** : **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** et **HttpDataChunkFromFragmentCache**, respectivement. Les réponses complètes dans le cache HTTP peuvent également être utilisées comme fragments dans la structure de [**\_ réponse http**](http-response.md) , bien que cette pratique ne soit pas recommandée.

La structure de [**\_ réponse http**](http-response.md) contient un pointeur vers un tableau de structures de [**\_ \_ blocs de données http**](/windows/desktop/api/Http/ns-http-http_data_chunk) qui constituent le corps d’entité de la réponse. La structure de **\_ réponse http** contient également un nombre correspondant qui spécifie la dimension du tableau de structures de **\_ \_ blocs de données http** . La valeur HttpDataChunkFromFragmentCache dans la structure de **\_ \_ segment de données http** spécifie le type de cache de fragment du segment de données. La structure de **\_ \_ segment de données http** spécifie également le nom du fragment.

Une réponse qui contient un fragment mis en cache échoue avec un \_ chemin d’erreur \_ \_ introuvable si l’une des entrées du cache de fragments n’est pas disponible. Étant donné que les entrées du cache de fragments ne sont pas nécessairement disponibles, les applications doivent être préparées pour gérer ce cas. Pour gérer ce cas, vous pouvez essayer d’ajouter à nouveau l’entrée du cache de fragment et de renvoyer la réponse. En cas de défaillances répétées, l’application peut utiliser des blocs de données stockés dans des mémoires tampons au lieu d’entrées de fragment du cache.

Les entrées du cache de fragments peuvent également être spécifiées dans la fonction [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) . Le fragment est ajouté au corps d’entité dans la structure de [**\_ \_ segment de données http**](/windows/desktop/api/Http/ns-http-http_data_chunk) comme décrit ci-dessus. Là encore, l’envoi peut échouer si l’une des entrées du cache de fragments spécifiée n’est pas disponible.

 

 





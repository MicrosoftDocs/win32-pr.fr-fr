---
description: Stratégies de communication avec plusieurs clients de canal et de maintenance de plusieurs instances de canal.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Instances de canal nommé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481960"
---
# <a name="named-pipe-instances"></a>Instances de canal nommé

Le serveur de canal le plus simple crée une seule instance d’un canal, se connecte à un client unique, communique avec le client, se déconnecte du client, ferme le handle de canal et se termine. Toutefois, il est plus courant pour un serveur de canal de communiquer avec plusieurs clients de canal. Un serveur de canaux peut utiliser une seule instance de canal pour se connecter à plusieurs clients de canal en se connectant et en se déconnectant de chaque client en séquence, mais les performances seraient médiocres. Le serveur de canaux doit créer plusieurs instances de canal pour gérer efficacement plusieurs clients simultanément.

Il existe trois stratégies de base pour traiter plusieurs instances de canal.

-   Créez un thread distinct pour chaque instance du canal. Pour obtenir un exemple de serveur de canaux multithread, consultez [serveur de canal multithread](multithreaded-pipe-server.md).
-   Utilisez des opérations avec chevauchement en spécifiant une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) dans les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Pour obtenir un exemple, consultez [serveur de canal nommé utilisant des e/s avec chevauchement](named-pipe-server-using-overlapped-i-o.md).
-   Utilisez des opérations avec chevauchement à l’aide des fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) , qui spécifient une routine de saisie semi-automatique à exécuter lorsque l’opération est terminée. Pour obtenir un exemple, consultez [serveur de canaux nommés utilisant les routines de saisie semi-automatique](named-pipe-server-using-completion-routines.md).

Le serveur de canal multithread est plus facile à écrire, car le thread de chaque instance gère les communications pour un client de canal unique. Le système alloue le temps processeur à chaque thread en fonction des besoins. Toutefois, chaque thread utilise des ressources système, ce qui est un inconvénient pour un serveur de canal qui gère un grand nombre de clients.

Avec un serveur à thread unique, il est plus facile de coordonner les opérations qui affectent plusieurs clients, et il est plus facile de protéger les ressources partagées d’un accès simultané par plusieurs clients. Le défi d’un serveur à thread unique est qu’il nécessite la coordination des opérations avec chevauchement pour allouer du temps processeur pour gérer les besoins simultanés des clients.

 

 

---
title: Routage des demandes entrantes
description: L’API du serveur HTTP gère une base de données de routage pour déterminer l’application qui reçoit une demande entrante.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40feab96a913da895633bddd8e53697b6aeef959162da054da22aeeedef652a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829959"
---
# <a name="routing-incoming-requests"></a>Routage des demandes entrantes

L’API du serveur HTTP gère une base de données de routage pour déterminer l’application qui reçoit une demande entrante. La table de routage est créée à partir de la base de données de réservation et contient des entrées de réservation ainsi que des inscriptions actuelles. Lorsqu’une inscription ou une réservation est effectuée, elle est placée dans le compartiment de la base de données de routage qui correspond au type d’hôte comme suit :

-   \+ : les inscriptions de port sont placées dans le compartiment « caractère générique fort ».

-   hôte : les inscriptions de port sont placées dans le compartiment « explicite »

-   IP : les inscriptions de port sont placées dans le compartiment « caractère générique faible lié à IP »

-   \* : les inscriptions de port sont placées dans le compartiment « caractère générique faible »

Ces étapes font également référence à l’ordre de traitement des demandes HTTP entrantes. En premier lieu, les réservations à caractères génériques fortes sont vérifiées, suivies du caractère générique faible lié à IP et du caractère générique faible. La recherche s’arrête lorsqu’une correspondance est trouvée afin que les inscriptions dans l’un des compartiments restants soient introuvables.

L’algorithme de routage de l’API du serveur HTTP localise la meilleure correspondance pour le [URLPrefix](urlprefix-strings.md) en effectuant une recherche dans les entrées d’inscription et les entrées de réservation de la base de données de routage, en commençant par le compartiment à caractères génériques renforcé et en terminant par la plage de caractères génériques faibles. La meilleure correspondance, au sein d’un compartiment, est la correspondance la plus longue dans la partie URI relative du UrlPrefix (en supposant une correspondance exacte pour les parties hôte, port et schéma de l’URL). Une fois qu’une correspondance a été trouvée dans un compartiment, l’algorithme de routage arrête sa recherche et ignore tous les compartiments de priorité inférieure.

Par exemple, considérez les inscriptions suivantes (classées par ordre de priorité décroissant selon les types de compartiments :

-   Inscription : `https://+:80/vroot/` est inscrit par l’application 1

-   Inscription : `https://adatum.com:80/` est inscrit par l’application 2

-   Inscription : `https://\*:80/` est inscrit par l’application 3

Une demande entrante pour `https://adatum.com:80/vroot/subdir/file.htm/` est remise à l’application 1. Une demande entrante pour `https://adatum.com:80/default.htm/` est remise à l’application 2. Une demande entrante pour `https://otheradatum.com:80/file.htm/` est remise à l’application 3.

Si la meilleure correspondance est une entrée de réservation, cela signifie que l’application qui doit recevoir la demande n’est pas en cours d’exécution. Par exemple, considérez l’inscription et la réservation suivantes :

-   Inscription : `https://\*:80/vroot/` est inscrit par l’application 1, utilisateur a

-   Réservation : `https://adatum.com:80/` a été réservé pour l’utilisateur B

Une demande entrante pour `https://adatum.com:80/vroot/file.htm/` n’est pas remise à l’application 1 car la meilleure correspondance correspond à l’entrée de réservation pour l’utilisateur B. Dans ce cas, les règles de précédence sont appliquées à la réservation qui a une priorité plus élevée. Si aucun processus actif n’est autorisé et inscrit aux demandes de service pour l’URL reçue, la demande est rejetée avec un code d’état 400 (demande incorrecte).

 

 





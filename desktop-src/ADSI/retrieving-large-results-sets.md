---
title: Récupération de jeux de résultats volumineux
description: Lorsque le jeu de résultats qui sera renvoyé peut contenir plus de 1000 éléments, vous devez utiliser une recherche paginée.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Récupération des ensembles de résultats volumineux (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122138"
---
# <a name="retrieving-large-results-sets"></a>Récupération de jeux de résultats volumineux

Lorsque le jeu de résultats qui sera renvoyé peut contenir plus de 1000 éléments, vous devez utiliser une recherche paginée. Les recherches de Active Directory effectuées sans pagination sont limitées au fait de retourner un maximum de 1000 premiers enregistrements. Avec une recherche paginée, le jeu de résultats est présenté sous la forme de pages individuelles, chacune contenant un nombre prédéterminé d’entrées de résultat. Avec ce type de recherche, de nouvelles pages d’entrées de résultats sont retournées jusqu’à ce que la fin du jeu de résultats soit atteinte.

Par défaut, le serveur qui répond à une demande de requête calcule complètement un jeu de résultats avant de retourner des données. Dans un jeu de résultats volumineux, la mémoire du serveur doit être utilisée lors de l’acquisition du jeu de résultats, et la bande passante réseau lorsque le résultat important est retourné. La définition d’une taille de page permet au serveur d’envoyer les données dans des pages au fur et à mesure que les pages sont générées. Le client met ensuite en cache ces données et fournit un curseur au code au niveau de l’application. La pagination est définie en définissant le nombre de lignes que le serveur calcule avant que les données ne soient retournées sur le réseau au client.

La recherche paginée offre des avantages au client et au serveur. Par exemple, le client peut être plus réactif dans la présentation des résultats aux utilisateurs finaux. Cela est particulièrement utile pour les outils d’interface utilisateur graphique qui peuvent afficher des données alors qu’un autre thread reçoit simultanément plus de données du serveur.

Quand vous configurez votre requête, si vous spécifiez un ordre de tri pour votre jeu de résultats, le serveur doit entièrement calculer le jeu de résultats avant de renvoyer les données au client, ce qui a un impact sur le temps de réponse de la requête.

Côté serveur, la recherche paginée rend l’opération évolutive. Par exemple, si les clients 100 émettent des demandes de recherche simultanément et, en moyenne, chaque client est renvoyé 200 objets, si la taille de page n’est pas spécifiée, le serveur doit disposer de suffisamment de mémoire pour contenir le jeu de résultats complet de 20 000 entrées. Sinon, si chaque client a spécifié une taille de page de dix objets, les besoins en mémoire sur le serveur seront réduits de 20.

> [!Note]  
> Tous les services d’annuaire ne prennent pas en charge les recherches paginées. Active Directory implémente l’architecture de taille de page.

 

De nombreux serveurs d’annuaire spécifient une limite administrative pour le nombre maximal d’objets qu’ils peuvent retourner si un client ne spécifie pas la taille de la page. Lorsque la limite administrative est atteinte, ADSI génère l’erreur Win32 **\_ \_ administration \_ Limit \_ a dépassé** Win32 Error.

Côté client, une recherche paginée permet à un client d’arrêter l’opération pendant qu’elle est toujours en cours. En revanche, dans une recherche non paginée, le client est bloqué jusqu’à ce que les données soient entièrement retournées, ou qu’une erreur se produise. Cela peut avoir un impact sur les performances du réseau si le jeu de résultats est plus grand et prend plus de temps que prévu.

Pour le compte du client, ADSI gère la taille de page en toute transparence. Le client n’a pas besoin de compter le nombre d’objets en cours. ADSI encapsule l’interaction du serveur pour le client. Du point de vue du client, la recherche retourne un jeu de résultats complet.

Pour plus d’informations sur l’utilisation de l’option de délai de recherche avec une interface de recherche spécifique, consultez :

-   [Pagination avec IDirectorySearch](paging-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

Une recherche paginée est transparente pour votre application, car l’interface ADSI continue à récupérer des pages de résultats supplémentaires jusqu’à ce qu’elle atteigne la fin du jeu de résultats ou la fin de la limite de temps que vous avez définie. Lorsque vous utilisez une recherche paginée, la limite de taille ne remplace pas la taille de la page. La limite de taille peut être utilisée uniquement lorsque vous récupérez un jeu de résultats qui contient moins de 1000 entrées.

 

 





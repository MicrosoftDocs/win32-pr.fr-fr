---
title: Ajout d’une réservation
description: La base de données de routage contient la liste des réservations.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104508190"
---
# <a name="adding-a-reservation"></a>Ajout d’une réservation

La base de données de routage contient la liste des réservations. La liste de réservation se compose des utilisateurs qui sont autorisés à accéder à l’espace de noms, ainsi que du niveau d’accès pour chaque utilisateur répertorié sous la réservation. Lorsque des réservations sont ajoutées ou supprimées, la base de données de routage est recherchée pour déterminer les privilèges d’accès.

En plus de vérifier l’ID des utilisateurs, l’API du serveur HTTP vérifie également la présence de conflits dans les réservations existantes avant d’installer une nouvelle réservation.

**Pour ajouter une nouvelle réservation**

1.  Si le numéro de port dans le UrlPrefix a des réservations ou des inscriptions pour un schéma différent du schéma dans le UrlPrefix, l’inscription échoue. Les protocoles HTTP et HTTPs ne peuvent pas être pris en charge sur le même port.
2.  Recherchez le compartiment approprié pour l’inscription (voir la section [routage des demandes entrantes](routing-incoming-requests.md) ), en fonction du type d’hôte. Les étapes restantes sont relatives à ce compartiment.
3.  Sélectionnez entrées de réservation avec les composants de schéma, d’hôte et de port qui correspondent au UrlPrefix réservé. À partir de celles-ci, localisez l’entrée ayant le *relativeUri* correspondant le plus long, qui n’est pas égal au relativeUri dans la réservation (autrement dit, le *nœud parent*). Si l’entrée existe, évaluez les droits d’accès en fonction de la liste de contrôle d’accès assignée à cette entrée.
4.  Si un nœud parent est introuvable, il s’agit d’une réservation avec un relativeUri vide ou une *réservation racine*. Accordez des droits d’accès uniquement si l’appelant est inscrit sous les comptes LocalSystem ou administrateur.
5.  Si des droits d’accès sont accordés, vérifiez les réservations en double. Si une entrée de réservation existe avec les mêmes schéma, port, hôte et relativeUri, le code d’une erreur \_ \_ existe déjà est retourné.
    > [!Note]  
    > La mise à jour d’une entrée existante doit être effectuée en deux étapes : supprimer l’entrée et en ajouter une nouvelle.

     

Si les étapes ci-dessus ont réussie, une nouvelle entrée de réservation est entrée dans la base de données de réservation.

> [!Note]  
> La nouvelle entrée est créée avec la liste de contrôle d’accès spécifiée et n’hérite pas des ACL de l’entrée *parente* .

 

Les exemples suivants illustrent le processus de réservation.

-   Réservation 1 : `https://+:80/vroot/subdir/` par l’administrateur de l’utilisateur A et l’utilisateur C parvient à entrer dans le compartiment « + ».
-   Réservation 2 : `https://adatum.com:80/vroot/` par l’administrateur pour l’utilisateur B et est entré dans le compartiment « hôte explicite ».
-   Réservation 3 : `https://adatum.com:80/vroot/subdir/otherdir/` par l’utilisateur B pour l’utilisateur C s’est correctement déroulée en raison de la réservation 2.
-   Réservation 4 : `https://+:80/vroot/subdir/otherdir/` par l’utilisateur A pour l’utilisateur E s’est correctement déroulée en raison de la réservation 1.
-   Réservation 5 : `https://adatum.com:80/vroot/subdir/otherdir/` par l’utilisateur A pour l’utilisateur E échoue. Accès refusé en raison de la réservation 2.
-   Réservation 6 : `https://+:80/vroot/subdir/` par l’administrateur de l’utilisateur A échoue. La réservation est en conflit avec la réservation 1.
-   Réservation 7 : `https://adatum.com:80/newroot/` par l’utilisateur a pour l’utilisateur a échoue. Accès refusé en raison d’une réservation racine implicite de `https://adatum.com:80/` pour LocalSystem ou administrateur.

Les réservations peuvent affecter le jeu d’URL dans les demandes remises à un processus qui a précédemment inscrit un UrlPrefix. Par exemple, considérez le scénario suivant.

-   Inscription : `https://adatum.com:80/vroot/` par application 1 pour l’utilisateur A.
-   Une demande pour `https://adatum.com:80/vroot/subdir/file.htm` est remise à l’application 1.
-   Réservation : `https://+:80/vroot/subdir/` pour l’utilisateur B.
-   Une requête pour `https://adatum.com:80/vroot/subdir/file.htm` est maintenant rejetée.
-   Inscription : `https://adatum.com:80/vroot/subdir/` par application 2 pour l’utilisateur B.
-   Une demande pour `https://adatum.com:80/vroot/subdir/file.htm` est remise à l’application 2.

 

 





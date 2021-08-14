---
title: Traitement des inscriptions
description: Les API de serveur HTTP utilisent la base de données de routage pour appliquer les vérifications d’accès pendant les inscriptions.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393842"
---
# <a name="processing-registrations"></a>Traitement des inscriptions

Les API de serveur HTTP utilisent la base de données de routage pour appliquer les vérifications d’accès pendant les inscriptions. Une inscription pour un [URLPrefix](urlprefix-strings.md) doit transmettre une série de vérifications d’accès pour s’assurer que l’utilisateur qui s’inscrit pour l’espace de noms dispose des droits d’accès. Utilisez la fonction [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) pour ajouter une nouvelle inscription.

**Pour ajouter une nouvelle inscription avec HttpAddUrl**

1.  Si le numéro de port dans le UrlPrefix a des réservations ou des inscriptions pour un schéma différent du schéma dans le UrlPrefix, l’inscription échoue. Les protocoles HTTP et HTTPs ne peuvent pas être pris en charge sur le même port.
2.  L’inscription est distante dans le compartiment approprié pour l’inscription. Les compartiments sont basés sur le type d’hôte de l’URL, comme indiqué dans la section [routage des demandes entrantes](routing-incoming-requests.md) . Les étapes suivantes sont relatives à ce compartiment particulier.
3.  Si une entrée d’inscription en double existe, retourne un code d’erreur.
4.  Sélectionnez entrées de réservation avec des composants de schéma, d’hôte et de port qui sont égaux à ceux de l’UrlPrefix. À partir de celles-ci, localisez l’entrée avec la correspondance **relativeUri** la plus longue. Si l’entrée existe, vérifiez les autorisations en fonction de la liste de contrôle d’accès associée à cette entrée et revenez à la réussite. Si l’entrée n’existe pas, retourne un code d’erreur \_ déjà \_ existant.

Les exemples suivants illustrent le processus d’installation d’une inscription dans la base de données de routage. Les réservations 1 et 2 existent dans la base de données de routage.

-   Réservation 1 : `https://+:80/vroot/subdir/` pour l’utilisateur A et l’utilisateur C. Cette réservation est placée dans le compartiment « + ».
-   Réservation 2 : `https://adatum.com:80/vroot/` pour l’utilisateur B. Cette réservation est placée dans le compartiment « hôte explicite ».
-   Inscription : `https://+:80/vroot/subdir/` par l’utilisateur B échoue en raison de la réservation 1.
-   Inscription : `https://adatum.com:80/vroot/subdir/` par l’utilisateur B a échoué en raison de la réservation 2.
-   Inscription : `https://adatum.com:80/vroot/subdir/` par l’utilisateur C échoue en raison de la réservation plus explicite 2. La réservation de caractères génériques forts n’a pas de sens dans le contexte de la réservation ou de l’inscription explicite.
-   Inscription : `https://+:80/vroot/subdir/` par l’utilisateur A s’est correctement déroulée en raison de la réservation 1.
-   Inscription : `https://adatum.com:80/vroot/anotherdir/` par l’utilisateur B a échoué en raison de la réservation 2.

Le contrôle d’accès pour l’inscription n’inclut pas les vérifications des privilèges de délégation. Il n’y a pas de contrôles d’accès basés sur des réservations (voir [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). La seule exigence pour supprimer une inscription au processus appelant doit avoir créé l’inscription.

 

 





---
description: Explique les moyens permettant à une application ou à un fournisseur de services de se connecter à une carte à puce à l’aide du sous-système de carte à puce.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Accès à une carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413485"
---
# <a name="accessing-a-smart-card"></a>Accès à une carte à puce

Le sous-système de [*carte à puce*](/windows/desktop/SecGloss/s-gly) offre plusieurs moyens permettant à une application ou à un [*fournisseur de services*](/windows/desktop/SecGloss/c-gly) de se connecter à une carte à puce :

-   Une application peut appeler [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) pour se connecter à une carte qui réside dans un lecteur donné. Il s’agit de la façon la plus simple d’établir une communication avec une carte à puce.
-   Une application peut rechercher une carte à puce spécifique au sein d’un groupe de lecteurs donné. L’application identifie la carte par son nom d’affichage et spécifie une liste de lecteurs dans laquelle la carte peut apparaître. Le [*Gestionnaire des ressources*](/windows/desktop/SecGloss/r-gly) recherche dans la liste de lecteurs toutes les cartes avec une [*chaîne ATR*](/windows/desktop/SecGloss/a-gly) qui correspond à la carte nommée et retourne les informations d’État à l’application. Le [*sous-système de carte à puce*](/windows/desktop/SecGloss/s-gly) ne met jamais une interface utilisateur graphique ou interagit avec la carte au-delà de l’obtention de la chaîne ATR. Toutefois, il fournit suffisamment d’informations pour que l’application ou un contrôle commun puisse guider l’utilisateur en localisant le type de carte ou de carte souhaité. Cela entraîne le mappage de la requête à un lecteur spécifique, vers lequel des e/s supplémentaires sont dirigées.
-   Une application peut demander une liste de cartes prenant en charge un ensemble donné d’interfaces de carte à puce. L’application peut ensuite utiliser la liste dans le cas précédent. Cela permet aux applications de se connecter à des cartes en fonction de leurs fonctionnalités, sans tenir compte de leurs noms.

Lorsqu’une application recherche une carte, elle fournit un tableau de noms de lecteurs dans lequel rechercher. Pour chaque élément lecteur du tableau, Resource Manager fournit les informations suivantes :

-   Indique si le lecteur est disponible pour une utilisation par cette application.
-   Si une carte est insérée dans ce lecteur et, le cas échéant, quelle est sa chaîne ATR.
-   Si la chaîne ATR de la carte correspond à l’une des chaînes ATR des cartes demandées.

L’application utilise les informations renvoyées pour appliquer des filtres supplémentaires aux cartes ou pour inviter l’utilisateur à sélectionner la carte de votre choix. Notez qu’une ou plusieurs des lecteurs de la liste renvoyée peuvent être ouverts pour une utilisation exclusive par d’autres applications. par conséquent, l’accès à cette liste de lecteurs n’est pas garanti.

 

 

---
description: Windows Composants homologues pour les personnes près de moi
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows Composants homologues pour les personnes près de moi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011497"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows Composants homologues pour les personnes près de moi

dans le principal Windows exécutable réseau pair à pair (P2phost.exe), l' [Architecture voisinage immédiat](people-near-me-architecture.md) utilise les composants suivants :

### <a name="people-near-me"></a>Voisinage immédiat

Le composant voisinage immédiat (PNM) initie la découverte à l’aide de la découverte de services Web sur le sous-réseau local pour les noms d’utilisateur des ordinateurs autorisés à PNM.

### <a name="people-near-me-publisher"></a>Voisinage immédiat Publisher

le composant voisinage immédiat Publisher publie les pseudos des utilisateurs connectés pour indiquer la disponibilité à d’autres ordinateurs à l’aide de PNM sur le sous-réseau local. L’utilisateur connecté doit choisir de publier son surnom avant qu’il ne soit publié. Le surnom est publié sur le sous-réseau à l’aide de la découverte de services Web. En outre, les objets et les applications peuvent également être publiés. Toutefois, l’utilisateur doit spécifier la publication de l’objet et de l’application pour les portées «**People Near me**» ou «**All**».

### <a name="people-near-me-enumerator"></a>Énumérateur voisinage immédiat

Le composant énumérateur voisinage immédiat énumère la liste des utilisateurs sur le sous-réseau local. À l’aide de cette liste, la découverte de services Web envoie une requête de multidiffusion et reçoit les réponses. Une fois la liste des surnoms obtenue, une application peut utiliser l’API pour récupérer plus de données publiées par l’utilisateur (qui est chiffré à l’aide de [Schannel](windows-vista-components-for-people-near-me.md)), telles que la liste des applications inscrites et les objets en cours de publication.

Le processus de recherche et d’énumération ne se produit pas automatiquement, mais doit être explicitement initié par un utilisateur ou une application en se connectant à PNM. Les résultats de la recherche sont la liste des diminutifs d’autres utilisateurs sur le même sous-réseau qui publient leurs surnoms à l’aide de l’API PNM.

### <a name="publication-manager"></a>Gestionnaire de publication

Le composant Gestionnaire de publication est responsable de la publication des mises à jour de la présence, de l’application ou des objets sur les contacts ou les personnes proches de l’abonnement ou de l’interrogation des données.

### <a name="peer-signaling"></a>Signalisation d’homologue

Le composant de signalement d’homologue gère la création de connexions entre homologues pour échanger des données. Pour voisinage immédiat, la signalisation d’homologue est utilisée lorsqu’un utilisateur ou une application envoie la requête de monodiffusion à un ordinateur spécifique pour sa clé publique, ses applications et ses objets.

### <a name="receive-invitation-handlerux"></a>Recevoir le gestionnaire d’invitation/UX

Le composant Gestionnaire d’invitation de réception/UX reçoit une invitation entrante d’une autre personne, invite l’utilisateur à déterminer s’il souhaite lancer l’application associée à l’invitation, puis lance l’application en fonction de l’utilisateur qui accepte l’invitation. Une invitation est un message d’une autre personne qui lance l’activité de collaboration à l’aide d’une application spécifique installée sur les ordinateurs des utilisateurs et publiée par l’utilisateur invité.

### <a name="peer-security"></a>Sécurité de l’homologue

Lorsque la présence, l’application et l’objet sont envoyés, les informations sont chiffrées à l’aide d’un canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)). L’ordinateur initiateur utilise la clé publique de l’ordinateur invité pour négocier une clé secrète utilisée pour chiffrer les données ultérieures envoyées entre les deux pairs.

 

 




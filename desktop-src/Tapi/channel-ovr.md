---
description: Chaque ligne possède un ou plusieurs canaux. Les fournisseurs de services gèrent normalement la manière dont les canaux sont exposés en tant qu’adresses à une application, et l’utilisateur final ou le serveur n’a pas besoin d’une connaissance spécifique des canaux.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233069"
---
# <a name="channel-telephony-api"></a>Canal (API de téléphonie)

Chaque ligne possède un ou plusieurs canaux. Les fournisseurs de services gèrent normalement la manière dont les canaux sont exposés en tant qu’adresses à une application, et l’utilisateur final ou le serveur n’a pas besoin d’une connaissance spécifique des canaux.

Les canaux sont identiques et sont donc interchangeables. Dans les POTS (Plain Old Telephone Service), il existe exactement un canal sur une ligne, et le canal est utilisé exclusivement pour la voix. Avec RNIS, au moins trois canaux (et plus de 30) canaux peuvent exister simultanément sur une ligne.

Chaque canal peut avoir sa propre adresse, ce qui signifie qu’une ligne peut avoir autant d’adresses qu’il y a de canaux. La relation exacte entre les canaux et les adresses exposées à une application dépend de l’implémentation d’un fournisseur de services.

Certains fournisseurs de services prennent en charge l’attribution de plusieurs adresses à un seul canal. Sur les lignes de POTS, plusieurs adresses sont rendues possibles par différents systèmes, tels que la numérotation directe (DID) ou la sonnerie distinctive, qui sont des services supplémentaires fournis par l’entreprise téléphonique.

De nombreuses grandes entreprises utilisent des appels entrants. Avant qu’un appel ne soit connecté, son numéro d’extension de destination est signalé au PBX, ce qui provoque l’appel de l’extension au lieu du téléphone de l’opérateur. Un exemple de sonneries distinctives dans une page d’hébergement privée serait si les parents utilisaient une adresse, les enfants une autre et un troisième pour le télécopieur. Étant donné qu’une seule ligne connecte la maison au réseau téléphonique, tous les téléphones sonnent lorsqu’un appel s’affiche, mais le modèle de sonnerie est différent selon le nombre que le tiers appelant a composé. Avec la sonnerie distinctive, les gens savent qui est l’appel entrant et l’ordinateur de télécopie répond à ses appels en reconnaissant son propre style de sonnerie.

Dans RNIS, les différents canaux B n’ont peut-être pas d’adresses distinctes. Étant donné que ces canaux B peuvent se trouver sur la même adresse, il s’agit du fournisseur de services (et non de l’application ou d’une personne qui a composé le numéro) qui attribue des appels à ces canaux.

 

 




---
description: Application des niveaux de gestion parentale
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Application des niveaux de gestion parentale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119941"
---
# <a name="enforcing-parental-management-levels"></a>Application des niveaux de gestion parentale

Tout titre ou partie d’un titre sur un disque DVD-Video peut se voir attribuer un niveau de gestion parental générique (PML) de 1 à 8. Lorsque le navigateur DVD lit le contenu qui a un PML, il est dit qu’il se trouve dans un *bloc parental*. Un bloc parental peut être constitué d’une partie d’un chapitre, de plusieurs chapitres ou de plusieurs titres. Une application DVD destinée à un marché international ne doit pas coder en dur un système d’évaluation particulier dans sa logique de gestion parentale.

Le navigateur DVD lui-même n’applique pas PMLs ; elle informe simplement votre application quand elle rencontre des informations PML sur le disque. Par défaut, il ignore ces informations sur le disque et lit le contenu de niveau le plus élevé. Pour appliquer le PMLs, votre application doit implémenter une forme de logique de contrôle de mot de passe qui associe les utilisateurs à des niveaux, demander au navigateur de DVD de l’envoyer aux notifications d’événements PML (en appelant la méthode [**IDvdControl2 :: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) au démarrage, avec les paramètres DVD \_ NotifyParentalLevelChange et **true**) et répondre à ces événements pour autoriser ou interdire l’accès selon les besoins.

Un titre de DVD peut avoir un PML global, mais les créateurs de disques peuvent attribuer à certaines sections de ce titre des PMLs plus ou moins restrictives. Il s’agit des commandes PML temporaires. ces commandes contiennent toujours deux instructions de branchement : une pour suivre si la commande PML temporaire est acceptée par l’application de lecteur, et l’autre pour suivre si la commande est rejetée. La séquence d’événements est la suivante. Le navigateur DVD lit le contenu vidéo (domaine du titre du DVD) lorsqu’il rencontre une commande PML temporaire sur le disque. Il vérifie son indicateur interne pour déterminer si l’application a demandé à être averti de cet événement. Si l’indicateur n’est pas défini, le DVD continue de fonctionner, en suivant la branche « modification du niveau parental rejetée » spécifiée sur le disque. Si l’indicateur est défini, le DVD envoie un \_ \_ \_ événement de changement de niveau parental du DVD EC \_ à l’application et attend un état de pause jusqu’à ce qu’il récupère une réponse. Lorsque votre application reçoit l’événement, elle utilise sa propre logique pour déterminer s’il faut accepter la commande. Il appelle ensuite [**IDvdControl2 :: AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) avec l’argument **true** ou **false**. Si la **valeur est true**, le navigateur DVD reprend son exécution, en suivant la branche « modification du niveau parental acceptée » spécifiée sur le disque. Dans le cas contraire, il reprend et suivent la branche « modification du niveau parental rejeté ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 




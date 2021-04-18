---
title: À propos de WER
description: Rapport d’erreurs Windows (WER) est une infrastructure de commentaires flexible basée sur les événements, conçue pour collecter des informations sur les problèmes matériels et logiciels que Windows peut détecter, signaler les informations à Microsoft et fournir aux utilisateurs toutes les solutions disponibles. Pour plus d’informations sur les améliorations apportées à WER, consultez What’s New in WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Rapport d’erreurs Windows Rapport d’erreurs Windows, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310493"
---
# <a name="about-wer"></a>À propos de WER

Rapport d’erreurs Windows (WER) est une infrastructure de commentaires flexible basée sur les événements, conçue pour collecter des informations sur les problèmes matériels et logiciels que Windows peut détecter, signaler les informations à Microsoft et fournir aux utilisateurs toutes les solutions disponibles. Pour plus d’informations sur les améliorations apportées à WER, consultez [What’s New in wer](what-s-new-in-wer.md).

À compter de Windows Vista, Windows fournit par défaut des erreurs de blocage, de réponse et de défaillance du noyau, sans nécessiter de modifications de votre application. Les applications utilisent à la place l’API WER pour générer des rapports d’erreurs pour les problèmes spécifiques à l’application qui ne sont pas liés aux incidents, aux non-réponses ou aux erreurs de noyau.

Pour générer des rapports d’erreurs pour les problèmes spécifiques à l’application, l’application doit créer une brève description du problème à l’aide de quelques informations de base appelées *paramètres de rapport*. Les paramètres de rapport comprennent des informations telles que le nom de l’application, la version de l’application, le nom du module, la version du module et le code d’erreur. La combinaison de ces paramètres de rapport décrit un problème unique.

Lorsque WER recherche une solution, il communique avec le serveur WER à Microsoft en lui demandant d’abord si le problème est déjà connu. Le serveur répond de l’une des manières suivantes :

-   Si le problème est connu et qu’il existe une solution, le serveur envoie la solution à l’ordinateur client et WER affiche ces informations à l’utilisateur.
-   Si le problème est étudié, le serveur peut envoyer une réponse qui indique l’État. Si le développeur a besoin d’informations supplémentaires pour résoudre le problème, le serveur demande des informations supplémentaires dans WER et WER demande à l’utilisateur l’autorisation d’envoyer ces informations.
-   Si le problème n’est pas connu, le serveur crée un problème pour qu’un développeur examine et envoie une réponse WER qui indique l’État.

À l’aide de ce processus, WER rassemble plus d’informations si nécessaire, ou envoie une solution à l’utilisateur lorsqu’il est disponible. Sur Windows Vista, l’utilisateur peut accéder aux **rapports et solutions aux problèmes** à tout moment pour afficher les solutions disponibles, vérifier si de nouvelles solutions sont disponibles ou gérer les autres rapports et paramètres wer. Sur Windows 7, les **rapports et solutions aux problèmes** sont désormais appelés **Centre de maintenance**. Cliquez sur **Démarrer** et entrez « afficher » dans **Rechercher les programmes et fichiers** , puis sélectionnez **Afficher tous les rapports de problèmes**, **afficher l’historique de fiabilité** ou afficher les **solutions aux problèmes**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rapport d’erreurs Windows](windows-error-reporting.md)
</dt> </dl>

 

 





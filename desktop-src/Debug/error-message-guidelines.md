---
description: Les instructions de cette rubrique sont destinées à vous aider à écrire des messages d’erreur clairs et faciles à localiser et utiles pour les clients.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Instructions relatives aux messages d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ceb2c89826ce45f39fdce2d0102e847c00245ba62ec3522e83725944b7f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343489"
---
# <a name="error-message-guidelines"></a>Instructions relatives aux messages d’erreur

Un message d’erreur est un texte qui s’affiche pour décrire un problème qui empêche l’utilisateur ou le système d’effectuer une tâche. Le problème peut entraîner une altération ou une perte de données. Les autres types de messages incluent les confirmations, les avertissements et les notifications. Les instructions de cette rubrique sont destinées à vous aider à écrire des messages d’erreur clairs et faciles à localiser et utiles pour les clients.

Les messages d’erreur mal écrits peuvent être une source de frustration pour les utilisateurs et peuvent augmenter les coûts de support technique. Un message d’erreur bien écrit fournit les informations suivantes à l’utilisateur :

-   Que s’est-il passé et pourquoi ?
-   Quel est le résultat final de l’utilisateur ?
-   Que peut faire l’utilisateur pour l’empêcher de se reproduire ?

La longueur du texte n’est pas un problème tant que le développeur gère correctement les tailles de mémoire tampon. Il est important que l’utilisateur dispose de toutes les informations nécessaires pour résoudre le problème. Si un message comporte plusieurs audiences, vous devrez peut-être fournir un texte distinct pour les administrateurs, les utilisateurs finaux et les développeurs.

## <a name="best-practices"></a>Meilleures pratiques

Voici les façons d’améliorer vos messages d’erreur :

-   Évitez les conditions d’erreur. Si vous pouvez prédire qu’une erreur se produit lorsqu’un utilisateur effectue une action spécifique, réécrivez votre code afin que l’utilisateur ne puisse pas provoquer l’erreur.
-   Écrivez un message d’erreur distinct pour chaque cause connue de l’erreur. N’utilisez pas un seul message générique pour expliquer chaque raison possible de l’erreur, sauf si vous ne pouvez pas déterminer la cause de l’erreur lorsqu’elle se produit.
-   Indiquez clairement le problème et, s’il s’avère utile pour l’utilisateur, expliquez ce qui a provoqué le problème. Dans la mesure du possible, remplacez les messages génériques des ressources de table de messages système par un message détaillé spécifique au problème.
-   Fournissez une solution au problème à l’utilisateur. Si la solution comporte plusieurs étapes, reportez-vous à la rubrique d’aide qui explique la tâche en détail.
-   Affiche uniquement le nom du produit, du composant ou de l’Assistant dans la barre de titre du message. Cela permet à l’utilisateur de déterminer où se trouve le problème. Ne résumez pas le problème dans la barre de titre ou incluez le mot « erreur ».
-   N’utilisez pas de jargon technique, utilisez la terminologie que votre auditoire comprend. N’utilisez pas l’argot ou les abréviations.
-   Utilisez les boutons de commande appropriés, tels que OK, annuler, oui, non et réessayer. Vous pouvez utiliser des combinaisons de ces boutons. Les boutons Oui et non doivent toujours être utilisés en combinaison et doivent toujours être précédés d’une question.
    -   Pour arrêter une opération et fermer la boîte de message, utilisez le bouton **Annuler** .
    -   Pour fermer une boîte de message, utilisez le bouton **Fermer** .
    -   Pour fournir plus d’informations sur la cause de l’erreur, utilisez le bouton **Détails** .
    -   Pour fournir plus d’informations sur la solution au problème, utilisez le bouton **aide** .
    -   Si une action de l’utilisateur est incluse dans le message, utilisez le bouton **OK** pour fermer la boîte de message.
    -   Les boutons **Oui** et **non** doivent être utilisés en combinaison et doivent toujours être précédés d’une question.
-   Si l’erreur est une erreur critique, écrivez-la dans le [Journal des événements](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Considérations relatives au style

-   Utilisez des phrases complètes mais simples.
-   Utilisez les dizaines de temps pour décrire les conditions qui ont provoqué le problème ou un État qui existe toujours. Vous pouvez utiliser le passé pour décrire un événement distinct qui s’est produit dans le passé.
-   Utilisez la voix active chaque fois que cela est possible. Vous pouvez utiliser la voix passive pour décrire la condition d’erreur.
-   Évitez les points d’exclamation et de texte en majuscules.
-   Ne vous exposez pas à l’erreur même si le problème est le résultat d’une erreur de l’utilisateur.
-   Ne pas anthropomorphize. N’Impliquez pas que les programmes ou le matériel peuvent avoir un sens ou un sentiment.
-   N’utilisez pas de mots ou d’expressions de langage commun. N’utilisez pas de termes pouvant être offensants dans certaines cultures.
-   Ne composez pas plusieurs noms sans ajouter de préposition ou de sous-clause pour clarifier la signification. Par exemple, « serveur d’annuaire du service LDAP du serveur de site » doit être remplacé par « serveur d’annuaire pour le service LDAP du serveur de site ».
-   Insérez des descripteurs avant un terme pour clarifier la signification de la phrase. Par exemple, « spécifier InfID quand la détection est définie sur non ». doit être remplacé par « spécifiez le paramètre InfID lorsque l’option détecter est définie sur non ».
-   Évitez le mot « Bad ». Utilisez des termes plus descriptifs pour indiquer à l’utilisateur ce qui est incorrect. Par exemple, évitez les messages tels que « taille incorrecte ». Au lieu de cela, indiquez à l’utilisateur les critères à utiliser lors de la spécification d’une taille.
-   Évitez le mot « veuillez ». Il peut être interprété pour signifier qu’une action requise est facultative.
-   Placez les mots à la fois dans l’index et pertinents à la signification centrale au début de la chaîne de message.

 

 

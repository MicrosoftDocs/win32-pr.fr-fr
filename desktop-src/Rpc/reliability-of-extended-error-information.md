---
title: Fiabilité des informations d’erreur étendues
description: Les informations d’erreur étendues ne sont pas fiables.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413621"
---
# <a name="reliability-of-extended-error-information"></a>Fiabilité des informations d’erreur étendues

Les informations d’erreur étendues ne sont pas fiables. Impossible d’utiliser les informations d’erreur étendues pour générer la logique du code. Il convient de vérifier la présence d’informations d’erreur étendues et, le cas échéant, de vider, d’enregistrer ou de consigner ces informations. Mais ne vous fiez pas aux informations ou à son contenu.

Les raisons suivantes expliquent pourquoi les informations d’erreur étendues ne sont pas fiables :

-   La séquence et le contenu des enregistrements d’erreurs étendus dépendent de l’architecture interne du système, qui est sujette à modification. Une certaine opération peut traverser NPFS sur les systèmes actuels, mais demain peut passer par TCP. Ces différents composants génèrent des codes d’erreur très différents, et les contrôles de code sont par conséquent peu fiables et non recommandés.
-   La propagation des informations d’erreur étendues peut être désactivée, comme expliqué précédemment. Si le code de détection est inclus, l’application ne fonctionnera probablement pas dans certains environnements.
-   La propagation des informations d’erreur étendues est effectuée de manière optimale. La propagation ou la génération d’informations d’erreur étendues peut échouer si la mémoire est insuffisante sur l’ordinateur pour traiter ou propager la chaîne. Dans ce cas, la chaîne est supprimée. Certains protocoles ont des longueurs limitées pour les paquets d’erreurs, car ils n’incluent généralement pas une grande quantité d’informations. Si la longueur de la chaîne dépasse la longueur autorisée du paquet, le temps d’exécution RPC commence à supprimer les informations de la chaîne en vue de faire tenir la chaîne dans le paquet. La durée d’exécution supprime d’abord les enregistrements, en commençant par l’avant-dernier, jusqu’à ce que seuls le premier et le dernier enregistrement soient conservés. Si la chaîne ne tient toujours pas dans un paquet, le temps d’exécution expose les paramètres de chaîne et les noms d’ordinateur. Si un paramètre de chaîne est supprimé, le type du paramètre est défini sur aucun. Si un enregistrement est supprimé, l’indicateur EEInfoNextRecordsMissing est défini dans l’enregistrement suivant, et EEInfoPreviousRecordsMissing est défini dans l’enregistrement précédent.

 

 





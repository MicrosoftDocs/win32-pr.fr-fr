---
title: Raccourcis et variantes de commande
description: Raccourcis et variantes de commande
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009566"
---
# <a name="command-shortcuts-and-variations"></a>Raccourcis et variantes de commande

Vous pouvez utiliser plusieurs raccourcis quand vous utilisez des commandes MCI. Ces raccourcis vous permettent d’utiliser un identificateur unique pour faire référence à tous les appareils ouverts par votre application, ou d’ouvrir un appareil sans émettre explicitement une commande [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).

Vous pouvez spécifier « All » ( \_ tous les \_ \_ ID d’appareil MCI) comme identificateur d’appareil pour toute commande qui ne retourne pas d’informations. Lorsque vous spécifiez « All », MCI envoie la commande de manière séquentielle à tous les appareils ouverts par l’application actuelle.

Par exemple, la commande [**Fermer**](close.md) « tout » ferme tous les appareils ouverts et la commande [**lire**](play.md) « tout » démarre la lecture de tous les appareils ouverts par l’application. Étant donné que le MCI envoie séquentiellement les commandes aux périphériques MCI, il existe un intervalle entre le moment où le premier et le dernier périphérique reçoit la commande.

L’utilisation de « All » est un moyen pratique de diffuser une commande sur tous vos appareils, mais vous ne devez pas vous en servir pour synchroniser les appareils. le délai entre les messages peut varier.

Lorsque vous émettez une commande et spécifiez un appareil qui n’est pas ouvert, MCI tente d’ouvrir l’appareil avant d’implémenter la commande. Les règles suivantes s’appliquent à l’ouverture automatique des appareils :

-   La fonctionnalité d’ouverture automatique fonctionne uniquement avec l’interface de chaîne de commande.
-   La fonctionnalité d’ouverture automatique échoue pour les commandes qui sont spécifiques aux pilotes de périphérique personnalisés.
-   Les appareils ouverts automatiquement ne répondent pas aux commandes qui utilisent « All » comme nom de périphérique.
-   La fonctionnalité d’ouverture automatique ne permet pas à votre application de spécifier l’indicateur « type ». Sans le nom de l’appareil, MCI détermine le nom de l’appareil à partir des entrées du Registre. Pour utiliser un appareil spécifique, vous pouvez combiner le nom de l’appareil avec le nom de fichier à l’aide du point d’exclamation, comme décrit dans la documentation de référence pour la commande [**ouvrir**](open.md) .

Si une application utilise la fonctionnalité d’ouverture automatique pour ouvrir un appareil, l’application doit vérifier la valeur de retour de chaque commande Open suivante pour vérifier que l’appareil est toujours ouvert. MCI ferme également automatiquement tous les appareils qu’il ouvre automatiquement. MCI ferme généralement un appareil dans les cas suivants :

-   La commande est terminée.
-   Vous abandonnez la commande.
-   Vous demandez une notification dans une commande ultérieure.
-   MCI détecte une défaillance.

 

 





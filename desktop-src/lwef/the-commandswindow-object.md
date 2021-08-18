---
title: Objet CommandsWindow
description: Objet CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336bdff598a75a9b0b07adabb11c271a45ca84940f528ebe082de17841592d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882463"
---
# <a name="the-commandswindow-object"></a>Objet CommandsWindow

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’objet [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) permet d’accéder aux propriétés de la fenêtre commandes vocales. La fenêtre commandes vocales est une ressource partagée principalement conçue pour permettre aux utilisateurs d’afficher des commandes compatibles avec la voix. Si la reconnaissance vocale est désactivée, la fenêtre commandes vocales s’affiche toujours, avec le texte « entrée vocale désactivée » (dans la langue du caractère). Si aucun moteur de reconnaissance vocale n’est installé qui correspond au paramètre de langue du caractère dans lequel la fenêtre s’affiche, « entrée vocale non disponible ». Si le client d’entrée-actif n’a pas défini de paramètres vocaux pour ses commandes et a désactivé les commandes vocales globales, la fenêtre affiche « aucune commande vocale ». Vous pouvez également interroger les propriétés de la fenêtre commandes vocales, que l’entrée vocale soit désactivée ou qu’un moteur de reconnaissance vocale compatible soit installé.

-   [Propriétés CommandsWindow](commandswindow-properties.md)

 

 
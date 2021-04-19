---
title: Objet CommandsWindow
description: Objet CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510673"
---
# <a name="the-commandswindow-object"></a>Objet CommandsWindow

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’objet [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) permet d’accéder aux propriétés de la fenêtre commandes vocales. La fenêtre commandes vocales est une ressource partagée principalement conçue pour permettre aux utilisateurs d’afficher des commandes compatibles avec la voix. Si la reconnaissance vocale est désactivée, la fenêtre commandes vocales s’affiche toujours, avec le texte « entrée vocale désactivée » (dans la langue du caractère). Si aucun moteur de reconnaissance vocale n’est installé qui correspond au paramètre de langue du caractère dans lequel la fenêtre s’affiche, « entrée vocale non disponible ». Si le client d’entrée-actif n’a pas défini de paramètres vocaux pour ses commandes et a désactivé les commandes vocales globales, la fenêtre affiche « aucune commande vocale ». Vous pouvez également interroger les propriétés de la fenêtre commandes vocales, que l’entrée vocale soit désactivée ou qu’un moteur de reconnaissance vocale compatible soit installé.

-   [Propriétés CommandsWindow](commandswindow-properties.md)

 

 
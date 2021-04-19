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
# <a name="the-commandswindow-object"></a><span data-ttu-id="7b405-103">Objet CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="7b405-103">The CommandsWindow Object</span></span>

<span data-ttu-id="7b405-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b405-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7b405-105">L’objet [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) permet d’accéder aux propriétés de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="7b405-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="7b405-106">La fenêtre commandes vocales est une ressource partagée principalement conçue pour permettre aux utilisateurs d’afficher des commandes compatibles avec la voix.</span><span class="sxs-lookup"><span data-stu-id="7b405-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="7b405-107">Si la reconnaissance vocale est désactivée, la fenêtre commandes vocales s’affiche toujours, avec le texte « entrée vocale désactivée » (dans la langue du caractère).</span><span class="sxs-lookup"><span data-stu-id="7b405-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="7b405-108">Si aucun moteur de reconnaissance vocale n’est installé qui correspond au paramètre de langue du caractère dans lequel la fenêtre s’affiche, « entrée vocale non disponible ».</span><span class="sxs-lookup"><span data-stu-id="7b405-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="7b405-109">Si le client d’entrée-actif n’a pas défini de paramètres vocaux pour ses commandes et a désactivé les commandes vocales globales, la fenêtre affiche « aucune commande vocale ».</span><span class="sxs-lookup"><span data-stu-id="7b405-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="7b405-110">Vous pouvez également interroger les propriétés de la fenêtre commandes vocales, que l’entrée vocale soit désactivée ou qu’un moteur de reconnaissance vocale compatible soit installé.</span><span class="sxs-lookup"><span data-stu-id="7b405-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="7b405-111">Propriétés CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="7b405-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 
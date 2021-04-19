---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509807"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

**IAgentCommandWindow** définit une interface qui permet aux applications de définir et d’interroger les propriétés de la fenêtre commandes vocales. La fenêtre commandes vocales est une ressource partagée principalement conçue pour permettre aux utilisateurs d’afficher des commandes compatibles avec la voix. Si la reconnaissance vocale est désactivée, la fenêtre commandes vocales s’affiche toujours, avec le texte « entrée vocale désactivée » (dans la langue du caractère). Si aucun moteur vocal qui correspond au paramètre de langue du caractère n’est installé, la fenêtre affiche « entrée vocale non disponible ». Si le client d’entrée-actif n’a pas défini de paramètres vocaux pour ses commandes et a désactivé les commandes vocales globales, la fenêtre affiche « aucune commande vocale ». Vous pouvez également interroger les propriétés de la fenêtre commandes vocales, que l’entrée vocale soit désactivée ou qu’un moteur de reconnaissance vocale compatible soit installé.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCommandWindow                             | Description                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Définit la valeur de la propriété [**visible**](visible-property.md) de la fenêtre commandes vocales.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Retourne la valeur de la propriété [**visible**](visible-property.md) de la fenêtre commandes vocales. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Retourne la position de la fenêtre commandes vocales.                                                  |
| [**GetSize,**](iagentcommandwindow--getsize.md)         | Retourne la taille de la fenêtre de commandes vocales.                                                      |



 

 

 





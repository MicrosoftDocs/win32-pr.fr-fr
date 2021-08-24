---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80509efbe4f9d6391b3ac6ffbdf5cb02580826fd1aa7a94f1536ba5706322606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105177"
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
| [**GetSize**](iagentcommandwindow--getsize.md)         | Retourne la taille de la fenêtre de commandes vocales.                                                      |



 

 

 





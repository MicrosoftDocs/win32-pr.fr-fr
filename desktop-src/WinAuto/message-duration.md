---
title: Paramètre de durée du message
description: Les applications utilisent généralement des fenêtres indépendantes pour afficher brièvement des messages de notification importants à l’utilisateur. Une application crée la fenêtre, l’affiche pour une durée définie par l’application, puis détruit la fenêtre.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2657f71c60a489fbedffdf2730dd37f388b749f27fa68ac57e039b2f27d5f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828287"
---
# <a name="message-duration-parameter"></a>Paramètre de durée du message

Les applications utilisent généralement des fenêtres indépendantes pour afficher brièvement des messages de notification importants à l’utilisateur. Une application crée la fenêtre, l’affiche pour une durée définie par l’application, puis détruit la fenêtre.

Étant donné que les utilisateurs ayant des troubles de la vision ou des conditions cognitives peuvent avoir besoin de plus de temps pour lire les fenêtres contextuelles de notification, les applications ne doivent pas coder en dur la durée. Au lieu de cela, une application doit définir la durée en fonction de la valeur du paramètre système **SPI \_ GETMESSAGEDURATION** . Pour récupérer ce paramètre, utilisez la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

Les applications de technologie d’assistance peuvent définir la durée du message en fonction de l’entrée utilisateur, en définissant le paramètre système **SPI \_ SETMESSAGEDURATION** .

 

 
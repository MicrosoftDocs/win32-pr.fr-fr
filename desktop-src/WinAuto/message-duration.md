---
title: Paramètre de durée du message
description: Les applications utilisent généralement des fenêtres indépendantes pour afficher brièvement des messages de notification importants à l’utilisateur. Une application crée la fenêtre, l’affiche pour une durée définie par l’application, puis détruit la fenêtre.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382082"
---
# <a name="message-duration-parameter"></a>Paramètre de durée du message

Les applications utilisent généralement des fenêtres indépendantes pour afficher brièvement des messages de notification importants à l’utilisateur. Une application crée la fenêtre, l’affiche pour une durée définie par l’application, puis détruit la fenêtre.

Étant donné que les utilisateurs ayant des troubles de la vision ou des conditions cognitives peuvent avoir besoin de plus de temps pour lire les fenêtres contextuelles de notification, les applications ne doivent pas coder en dur la durée. Au lieu de cela, une application doit définir la durée en fonction de la valeur du paramètre système **SPI \_ GETMESSAGEDURATION** . Pour récupérer ce paramètre, utilisez la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

Les applications de technologie d’assistance peuvent définir la durée du message en fonction de l’entrée utilisateur, en définissant le paramètre système **SPI \_ SETMESSAGEDURATION** .

 

 
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
# <a name="message-duration-parameter"></a><span data-ttu-id="43864-104">Paramètre de durée du message</span><span class="sxs-lookup"><span data-stu-id="43864-104">Message duration parameter</span></span>

<span data-ttu-id="43864-105">Les applications utilisent généralement des fenêtres indépendantes pour afficher brièvement des messages de notification importants à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="43864-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="43864-106">Une application crée la fenêtre, l’affiche pour une durée définie par l’application, puis détruit la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="43864-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="43864-107">Étant donné que les utilisateurs ayant des troubles de la vision ou des conditions cognitives peuvent avoir besoin de plus de temps pour lire les fenêtres contextuelles de notification, les applications ne doivent pas coder en dur la durée.</span><span class="sxs-lookup"><span data-stu-id="43864-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="43864-108">Au lieu de cela, une application doit définir la durée en fonction de la valeur du paramètre système **SPI \_ GETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="43864-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="43864-109">Pour récupérer ce paramètre, utilisez la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="43864-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="43864-110">Les applications de technologie d’assistance peuvent définir la durée du message en fonction de l’entrée utilisateur, en définissant le paramètre système **SPI \_ SETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="43864-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 
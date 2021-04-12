---
description: Configuration
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuration (Windows et messages)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210070"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="528fd-103">Configuration (Windows et messages)</span><span class="sxs-lookup"><span data-stu-id="528fd-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="528fd-104">Les *éléments d’affichage* sont les parties d’une fenêtre et l’affichage qui s’affichent sur l’écran d’affichage du système.</span><span class="sxs-lookup"><span data-stu-id="528fd-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="528fd-105">Les *métriques du système* sont les dimensions de différents éléments d’affichage.</span><span class="sxs-lookup"><span data-stu-id="528fd-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="528fd-106">Les métriques système typiques incluent la largeur de la bordure de la fenêtre, la hauteur de l’icône, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="528fd-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="528fd-107">Les métriques système décrivent également d’autres aspects du système, par exemple si une souris est installée, si des caractères codés sur deux octets sont pris en charge ou si une version de débogage du système d’exploitation est installée.</span><span class="sxs-lookup"><span data-stu-id="528fd-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="528fd-108">La fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) récupère la métrique système spécifiée.</span><span class="sxs-lookup"><span data-stu-id="528fd-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="528fd-109">Les applications peuvent également récupérer et définir la couleur des éléments de fenêtre tels que les menus, les barres de défilement et les boutons à l’aide des fonctions [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) et [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="528fd-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="528fd-110">La fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) récupère ou définit différents attributs système, tels que l’heure du double-clic, le délai d’attente de l’économiseur d’écran, la largeur de la bordure de la fenêtre et le modèle de bureau.</span><span class="sxs-lookup"><span data-stu-id="528fd-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="528fd-111">Quand une application utilise **SystemParametersInfo** pour définir un paramètre, la modification a lieu immédiatement.</span><span class="sxs-lookup"><span data-stu-id="528fd-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="528fd-112">Cette fonction permet également aux applications de mettre à jour le profil utilisateur, de sorte que les modifications apportées au système sont conservées lors du redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="528fd-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 

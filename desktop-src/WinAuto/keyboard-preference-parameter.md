---
title: Paramètre de préférence du clavier
description: Le paramètre de préférence clavier indique que l’utilisateur s’appuie sur le clavier au lieu de la souris, de sorte que les applications doivent afficher les interfaces de clavier qui seraient autrement masquées.
ms.assetid: dc3c02d2-a350-4a86-a0b0-9dbb83880029
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802d4ff76efae985cc07b6fe42f9d6b53cdf0b53
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382202"
---
# <a name="keyboard-preference-parameter"></a><span data-ttu-id="0b454-103">Paramètre de préférence du clavier</span><span class="sxs-lookup"><span data-stu-id="0b454-103">Keyboard preference parameter</span></span>

<span data-ttu-id="0b454-104">Le paramètre de préférence clavier indique que l’utilisateur s’appuie sur le clavier au lieu de la souris, de sorte que les applications doivent afficher les interfaces de clavier qui seraient autrement masquées.</span><span class="sxs-lookup"><span data-stu-id="0b454-104">The keyboard preference parameter indicates that the user relies on the keyboard instead of the mouse, so applications should display keyboard interfaces that would otherwise be hidden.</span></span>

<span data-ttu-id="0b454-105">L’utilisateur contrôle la définition du paramètre de préférence clavier à l’aide de l’option Options d’ergonomie du panneau de configuration, ou d’une autre application pour la personnalisation de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="0b454-105">The user controls the setting of the keyboard preference parameter by using the Ease of Access Center in Control Panel, or another application for customizing the environment.</span></span> <span data-ttu-id="0b454-106">Les applications utilisent les indicateurs **SPI \_ GETKEYBOARDPREF** et **SPI \_ SETKEYBOARDPREF** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de préférence de clavier.</span><span class="sxs-lookup"><span data-stu-id="0b454-106">Applications use the **SPI\_GETKEYBOARDPREF** and **SPI\_SETKEYBOARDPREF** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the keyboard preference parameter.</span></span>

<span data-ttu-id="0b454-107">En outre, sur Windows 2000, les utilisateurs peuvent définir un paramètre qui indique si les touches d’accès de menu sont toujours soulignées.</span><span class="sxs-lookup"><span data-stu-id="0b454-107">Additionally, on Windows 2000, users can set a parameter that indicates whether menu access keys are always underlined.</span></span> <span data-ttu-id="0b454-108">Les applications utilisent les indicateurs **SPI \_ GETMENUUNDERLINES** et **SPI \_ SETMENUUNDERLINES** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de soulignement de menu.</span><span class="sxs-lookup"><span data-stu-id="0b454-108">Applications use the **SPI\_GETMENUUNDERLINES** and **SPI\_SETMENUUNDERLINES** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the menu underlines parameter.</span></span>

<span data-ttu-id="0b454-109">Quand une application reçoit un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) pour le paramètre de la préférence du clavier ou du menu de soulignement, il est recommandé que l’application appelle [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour mettre à jour les informations pour les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="0b454-109">When an application receives a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message for either the keyboard preference or menu underline parameter, it is recommended that the application call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) to update the information for both parameters.</span></span>

<span data-ttu-id="0b454-110">Notez que **SPI \_ GETMENUUNDERLINES** est identique à **SPI \_ GETKEYBOARDCUES**, et que **SPI \_ SETMENUUNDERLINES** est identique à **SPI \_ SETKEYBOARDCUES**.</span><span class="sxs-lookup"><span data-stu-id="0b454-110">Note that **SPI\_GETMENUUNDERLINES** is the same as **SPI\_GETKEYBOARDCUES**, and **SPI\_SETMENUUNDERLINES** is the same as **SPI\_SETKEYBOARDCUES**.</span></span>

 

 
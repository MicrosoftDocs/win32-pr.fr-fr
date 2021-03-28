---
description: 'Les fonctions suivantes permettent à une application d’enregistrer, de restaurer et de réinitialiser un contexte de périphérique : SaveDC, RestoreDC et ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Enregistrement, restauration et réinitialisation d’un contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973267"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a><span data-ttu-id="8dfdd-103">Enregistrement, restauration et réinitialisation d’un contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="8dfdd-103">Saving, Restoring, and Resetting a Device Context</span></span>

<span data-ttu-id="8dfdd-104">Les fonctions suivantes permettent à une application d’enregistrer, de restaurer et de réinitialiser un contexte de périphérique : [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)et [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span><span class="sxs-lookup"><span data-stu-id="8dfdd-104">The following functions enable an application to save, restore, and reset a device context: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc), and [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca).</span></span> <span data-ttu-id="8dfdd-105">La fonction SaveDC enregistre sur une pile GDI spéciale les objets graphiques du DC actuel et leurs attributs, ainsi que les modes graphiques.</span><span class="sxs-lookup"><span data-stu-id="8dfdd-105">The SaveDC function records on a special GDI stack the current DC's graphic objects and their attributes, and graphic modes.</span></span> <span data-ttu-id="8dfdd-106">Une application de dessin peut appeler cette fonction avant que l’utilisateur commence à dessiner et à enregistrer l’état d’origine de l’application, ce qui fournit une ardoise propre à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8dfdd-106">A drawing application can call this function before a user begins drawing and save the application's original state providing a clean slate for the user.</span></span> <span data-ttu-id="8dfdd-107">Pour revenir à cet état d’origine, l’application appelle la fonction RestoreDC.</span><span class="sxs-lookup"><span data-stu-id="8dfdd-107">To return to this original state, the application calls the RestoreDC function.</span></span>

<span data-ttu-id="8dfdd-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) est fourni pour réinitialiser les données DC de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="8dfdd-108">[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) is provided to reset printer DC data.</span></span> <span data-ttu-id="8dfdd-109">Une application appelle cette fonction pour réinitialiser l’orientation du papier, le format de papier, le facteur d’échelle de sortie, le nombre de copies à imprimer, la source de papier (ou l’emplacement), le mode duplex, etc.</span><span class="sxs-lookup"><span data-stu-id="8dfdd-109">An application calls this function to reset the paper orientation, paper size, output scaling factor, number of copies to be printed, paper source (or bin), duplex mode, and so on.</span></span> <span data-ttu-id="8dfdd-110">En règle générale, une application appelle cette fonction après qu’un utilisateur a modifié l’une des options d’imprimante et que le système a émis un message [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfdd-110">Typically, an application calls this function after a user has changed one of the printer options and the system has issued a [**WM\_DEVMODECHANGE**](wm-devmodechange.md) message.</span></span>

 

 




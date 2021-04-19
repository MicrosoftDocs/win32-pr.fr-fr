---
description: Description des techniques sous-standard pour l’exposition de contrôles personnalisés.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Techniques substandardistes pour l’exposition de contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541898"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="64e41-103">Techniques substandardistes pour l’exposition de contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="64e41-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="64e41-104">Si une application ne prend pas en charge Microsoft Active Accessibility, elle peut ne pas être entièrement accessible.</span><span class="sxs-lookup"><span data-stu-id="64e41-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="64e41-105">Les techniques suivantes rendent les contrôles partiellement compatibles :</span><span class="sxs-lookup"><span data-stu-id="64e41-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="64e41-106">Retourne une chaîne descriptive lorsque le contrôle est interrogé à l’aide du \_ message WM GETTEXT.</span><span class="sxs-lookup"><span data-stu-id="64e41-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="64e41-107">Par exemple, vous pouvez autoriser un équivalent personnalisé d’un contrôle bouton intitulé « imprimer » pour retourner la chaîne « bouton imprimer ».</span><span class="sxs-lookup"><span data-stu-id="64e41-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="64e41-108">Cela identifie le type de contrôle et l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="64e41-108">This identifies both control type and label.</span></span> <span data-ttu-id="64e41-109">La même chaîne est appropriée pour un bouton avec une étiquette autre que du texte, tel qu’un graphique d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="64e41-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="64e41-110">De même, autoriser un contrôle personnalisé qui se comporte comme une case à cocher pour retourner la chaîne de légende « impression activée, activée ».</span><span class="sxs-lookup"><span data-stu-id="64e41-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="64e41-111">Prenez en charge le \_ message WM GETDLGCODE, en identifiant l’entrée au clavier prise en charge.</span><span class="sxs-lookup"><span data-stu-id="64e41-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="64e41-112">Par exemple, autorisez un équivalent personnalisé d’un contrôle d’édition à gérer WM \_ GETDLGCODE en retournant DLGC \_ HASSETSEL s’il gère les messages pour définir la sélection, DLGC \_ WANTARROWS s’il utilise des touches de direction et DLGC \_ WANTCHARS pour indiquer qu’il utilise l’entrée de caractères.</span><span class="sxs-lookup"><span data-stu-id="64e41-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="64e41-113">Seuls les contrôles qui ont leurs propres handles de fenêtre peuvent répondre aux \_ messages WM GETTEXT et WM \_ GETDLGCODE.</span><span class="sxs-lookup"><span data-stu-id="64e41-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="64e41-114">Pour éviter les problèmes de compatibilité avec les aides à l’accessibilité, vous devez suivre Active Accessibility instructions avec soin lors de la conception de contrôles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="64e41-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="64e41-115">Pour plus d’informations sur la façon d’éviter des problèmes de compatibilité avec les aides à l’accessibilité, consultez la section [accessibilité](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="64e41-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 

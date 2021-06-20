---
title: Fenêtre Options des caractères avancés (fenêtre commandes vocales)
description: En savoir plus sur la fenêtre Options de caractères avancés, qui fournit des options permettant aux utilisateurs d’ajuster leur interaction avec tous les caractères.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404356"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="6ada1-103">Fenêtre Options des caractères avancés (fenêtre commandes vocales)</span><span class="sxs-lookup"><span data-stu-id="6ada1-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="6ada1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ada1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6ada1-105">La fenêtre Options de caractères avancés fournit des options permettant aux utilisateurs d’ajuster leur interaction avec tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="6ada1-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="6ada1-106">Par exemple, les utilisateurs peuvent désactiver l’entrée vocale ou modifier les paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6ada1-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="6ada1-107">Les utilisateurs peuvent également modifier les paramètres de sortie du mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="6ada1-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="6ada1-108">Ces paramètres remplacent tous les jeux par une application cliente ou définis dans le cadre de la définition des caractères.</span><span class="sxs-lookup"><span data-stu-id="6ada1-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="6ada1-109">Votre application ne peut pas modifier ou désactiver ces options, car elles s’appliquent aux préférences de l’utilisateur général pour le fonctionnement de tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="6ada1-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="6ada1-110">Toutefois, le serveur notifie votre application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) lorsque l’utilisateur modifie et applique une option.</span><span class="sxs-lookup"><span data-stu-id="6ada1-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="6ada1-111">Vous pouvez également afficher ou fermer la fenêtre à l’aide de la propriété [**visible**](visible-property.md) de la fenêtre et accéder à son emplacement par le biais de ses propriétés [**Top**](top-property.md) et [**Left**](left-property.md) .</span><span class="sxs-lookup"><span data-stu-id="6ada1-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="6ada1-112">Outre la prise en charge de l’animation d’un caractère, Microsoft agent prend en charge la sortie audio pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="6ada1-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="6ada1-113">Cela comprend la sortie orale et les effets sonores.</span><span class="sxs-lookup"><span data-stu-id="6ada1-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="6ada1-114">Pour une sortie orale, le serveur consigne automatiquement les images de la bouche définies du caractère dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="6ada1-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="6ada1-115">Vous pouvez choisir la synthèse TTS (conversion de texte par synthèse vocale), l’audio enregistré ou uniquement la sortie de texte de la bulle.</span><span class="sxs-lookup"><span data-stu-id="6ada1-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 





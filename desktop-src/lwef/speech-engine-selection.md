---
title: Sélection du moteur de reconnaissance vocale
description: Sélection du moteur de reconnaissance vocale
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839862"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="346f7-103">Sélection du moteur de reconnaissance vocale</span><span class="sxs-lookup"><span data-stu-id="346f7-103">Speech Engine Selection</span></span>

<span data-ttu-id="346f7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="346f7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="346f7-105">Le paramètre ID de langue d’un caractère détermine son langage d’entrée vocale par défaut. Microsoft Agent demande SAPI pour un moteur installé qui correspond à cette langue.</span><span class="sxs-lookup"><span data-stu-id="346f7-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="346f7-106">Si une application cliente ne spécifie pas de préférence de langue, Microsoft Agent tente de trouver un moteur de reconnaissance vocale qui correspond à l’ID de langue par défaut de l’utilisateur (à l’aide de l’ID de langue majeur, puis de l’ID de langue mineure).</span><span class="sxs-lookup"><span data-stu-id="346f7-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="346f7-107">Si aucun moteur ne correspond à cette langue, la reconnaissance vocale est désactivée pour ce caractère.</span><span class="sxs-lookup"><span data-stu-id="346f7-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="346f7-108">Vous pouvez également demander un moteur de reconnaissance vocale spécifique en spécifiant son ID de mode (à l’aide de la propriété Character [**SRModeID**](srmodeid-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="346f7-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="346f7-109">Toutefois, si l’ID de langue de cet ID de mode ne correspond pas au paramètre de langue du client, l’appel échoue (génère une erreur dans le contrôle).</span><span class="sxs-lookup"><span data-stu-id="346f7-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="346f7-110">Le moteur de reconnaissance vocale conserve alors le dernier moteur correctement défini par le client, ou s’il n’en a pas, le moteur qui correspond à l’ID de langue du système actuel.</span><span class="sxs-lookup"><span data-stu-id="346f7-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="346f7-111">S’il n’y a toujours aucune correspondance, l’entrée vocale n’est pas disponible pour ce client.</span><span class="sxs-lookup"><span data-stu-id="346f7-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="346f7-112">Microsoft agent charge automatiquement un moteur de reconnaissance vocale lorsque l’entrée vocale est lancée par un utilisateur en appuyant sur la touche d’écoute ou lorsque le client d’entrée-actif appelle la méthode [**Listen**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="346f7-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="346f7-113">Toutefois, un moteur peut également être chargé lors de la définition ou de l’interrogation de son ID de mode, lors de la définition ou de l’interrogation des propriétés de la fenêtre commandes vocales, lors de l’interrogation de [**SRStatus**](srstatus-property.md)ou lorsque la reconnaissance vocale est activée et que l’utilisateur affiche la page d’entrée vocale des options de caractères avancés.</span><span class="sxs-lookup"><span data-stu-id="346f7-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="346f7-114">Toutefois, Microsoft Agent ne continue de charger que les moteurs de reconnaissance vocale que les clients utilisent.</span><span class="sxs-lookup"><span data-stu-id="346f7-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 





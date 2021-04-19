---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509807"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="faee9-103">IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="faee9-103">IAgentCommandWindow</span></span>

<span data-ttu-id="faee9-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="faee9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="faee9-105">**IAgentCommandWindow** définit une interface qui permet aux applications de définir et d’interroger les propriétés de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="faee9-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="faee9-106">La fenêtre commandes vocales est une ressource partagée principalement conçue pour permettre aux utilisateurs d’afficher des commandes compatibles avec la voix.</span><span class="sxs-lookup"><span data-stu-id="faee9-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="faee9-107">Si la reconnaissance vocale est désactivée, la fenêtre commandes vocales s’affiche toujours, avec le texte « entrée vocale désactivée » (dans la langue du caractère).</span><span class="sxs-lookup"><span data-stu-id="faee9-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="faee9-108">Si aucun moteur vocal qui correspond au paramètre de langue du caractère n’est installé, la fenêtre affiche « entrée vocale non disponible ».</span><span class="sxs-lookup"><span data-stu-id="faee9-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="faee9-109">Si le client d’entrée-actif n’a pas défini de paramètres vocaux pour ses commandes et a désactivé les commandes vocales globales, la fenêtre affiche « aucune commande vocale ».</span><span class="sxs-lookup"><span data-stu-id="faee9-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="faee9-110">Vous pouvez également interroger les propriétés de la fenêtre commandes vocales, que l’entrée vocale soit désactivée ou qu’un moteur de reconnaissance vocale compatible soit installé.</span><span class="sxs-lookup"><span data-stu-id="faee9-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="faee9-111">**Méthodes dans l'ordre Vtable**</span><span class="sxs-lookup"><span data-stu-id="faee9-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="faee9-112">Méthodes IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="faee9-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="faee9-113">Description</span><span class="sxs-lookup"><span data-stu-id="faee9-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faee9-114">**SetVisible**</span><span class="sxs-lookup"><span data-stu-id="faee9-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="faee9-115">Définit la valeur de la propriété [**visible**](visible-property.md) de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="faee9-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="faee9-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="faee9-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="faee9-117">Retourne la valeur de la propriété [**visible**](visible-property.md) de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="faee9-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="faee9-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="faee9-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="faee9-119">Retourne la position de la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="faee9-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="faee9-120">**GetSize,**</span><span class="sxs-lookup"><span data-stu-id="faee9-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="faee9-121">Retourne la taille de la fenêtre de commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="faee9-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 





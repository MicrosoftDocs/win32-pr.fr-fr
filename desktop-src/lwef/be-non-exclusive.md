---
title: Être non exclusif
description: Être non exclusif
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379772"
---
# <a name="be-non-exclusive"></a><span data-ttu-id="0b688-103">Être non exclusif</span><span class="sxs-lookup"><span data-stu-id="0b688-103">Be Non-Exclusive</span></span>

<span data-ttu-id="0b688-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b688-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0b688-105">Les caractères interactifs peuvent être utilisés dans l’interface utilisateur en tant qu’assistants, guides, artisteseurs, réciteurs, agents commerciaux ou dans divers autres rôles.</span><span class="sxs-lookup"><span data-stu-id="0b688-105">Interactive characters can be employed in the user interface as assistants, guides, entertainers, storytellers, sales agents, or in a variety of other roles.</span></span> <span data-ttu-id="0b688-106">Un caractère qui effectue ou aide automatiquement ne doit pas être conçu de façon contraire au principe de conception permettant de garder le contrôle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b688-106">A character that automatically performs or assists should not be designed contrary to the design principle of keeping the user in control.</span></span> <span data-ttu-id="0b688-107">Lorsque vous ajoutez un caractère à l’interface d’un site Web ou d’une application conventionnelle, utilisez le caractère comme une amélioration plutôt qu’un remplacement de l’interface principale.</span><span class="sxs-lookup"><span data-stu-id="0b688-107">When adding a character to the interface of a website or conventional application, use the character as an enhancement, rather than a replacement of, the primary interface.</span></span> <span data-ttu-id="0b688-108">Évitez d’implémenter une fonctionnalité ou une opération qui requiert en exclusivité un caractère.</span><span class="sxs-lookup"><span data-stu-id="0b688-108">Avoid implementing any feature or operation that exclusively requires a character.</span></span>

<span data-ttu-id="0b688-109">De même, permettez à l’utilisateur de choisir le moment où il souhaite interagir avec votre caractère.</span><span class="sxs-lookup"><span data-stu-id="0b688-109">Similarly, let the user choose when they want to interact with your character.</span></span> <span data-ttu-id="0b688-110">Un utilisateur doit être en mesure de faire disparaître le caractère et de le faire retourner uniquement avec l’autorisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b688-110">A user should be able to dismiss the character and have it return only with the user's permission.</span></span> <span data-ttu-id="0b688-111">L’interaction forcée des caractères sur les utilisateurs peut avoir un effet négatif sérieux.</span><span class="sxs-lookup"><span data-stu-id="0b688-111">Forcing character interaction on users can have a serious negative effect.</span></span> <span data-ttu-id="0b688-112">Pour prendre en charge le contrôle utilisateur de l’interaction de caractères, Microsoft Agent comprend automatiquement les commandes masquer et afficher.</span><span class="sxs-lookup"><span data-stu-id="0b688-112">To support user control of character interaction, Microsoft Agent automatically includes Hide and Show commands.</span></span> <span data-ttu-id="0b688-113">L’API Microsoft agent prend également en charge ces méthodes. vous pouvez donc inclure la prise en charge de ces fonctions dans votre propre interface.</span><span class="sxs-lookup"><span data-stu-id="0b688-113">The Microsoft Agent API also supports these methods, so you can include support for these functions in your own interface.</span></span> <span data-ttu-id="0b688-114">En outre, l’interface utilisateur de Microsoft Agent comprend des propriétés globales qui permettent à l’utilisateur de remplacer certaines options de sortie de caractères.</span><span class="sxs-lookup"><span data-stu-id="0b688-114">In addition, Microsoft Agent's user interface includes global properties that enable the user to override certain character output options.</span></span> <span data-ttu-id="0b688-115">Pour vous assurer que les préférences de l’utilisateur sont conservées, ces propriétés ne peuvent pas être remplacées par le biais de l’API.</span><span class="sxs-lookup"><span data-stu-id="0b688-115">To ensure that the user's preferences are maintained, these properties cannot be overridden through the API.</span></span>

 

 





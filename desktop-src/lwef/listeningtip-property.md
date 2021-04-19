---
title: Propriété ListeningTip
description: Propriété ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543040"
---
# <a name="listeningtip-property"></a><span data-ttu-id="5f4a2-103">Propriété ListeningTip</span><span class="sxs-lookup"><span data-stu-id="5f4a2-103">ListeningTip Property</span></span>

<span data-ttu-id="5f4a2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f4a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5f4a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5f4a2-106">Retourne une valeur booléenne indiquant le paramètre de l’utilisateur actuel pour l’info-bulle d’écoute.</span><span class="sxs-lookup"><span data-stu-id="5f4a2-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="5f4a2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="5f4a2-108">*agent \* \* *. SpeechInput.ListeningTip**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="5f4a2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f4a2-109">Value</span></span>     | <span data-ttu-id="5f4a2-110">Description</span><span class="sxs-lookup"><span data-stu-id="5f4a2-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="5f4a2-111">**True**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-111">**True**</span></span>  | <span data-ttu-id="5f4a2-112">L’info-bulle d’écoute est activée.</span><span class="sxs-lookup"><span data-stu-id="5f4a2-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="5f4a2-113">**False**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-113">**False**</span></span> | <span data-ttu-id="5f4a2-114">L’info-bulle d’écoute est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5f4a2-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f4a2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5f4a2-115">Remarks</span></span>

<span data-ttu-id="5f4a2-116">La propriété **ListeningTip** indique si l’option Afficher l’info-bulle d’écoute dans la feuille de propriétés de l’agent Microsoft (options de caractères avancés) est activée.</span><span class="sxs-lookup"><span data-stu-id="5f4a2-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="5f4a2-117">Quand **ListeningTip** retourne la **valeur true** et que l’entrée vocale est activée, le serveur affiche la fenêtre d’info-bulle lorsque l’utilisateur appuie sur la touche d’écoute.</span><span class="sxs-lookup"><span data-stu-id="5f4a2-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f4a2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f4a2-118">See Also</span></span>

[<span data-ttu-id="5f4a2-119">**Événement AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="5f4a2-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 





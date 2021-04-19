---
title: Propriété SoundEffects
description: Propriété SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513662"
---
# <a name="soundeffects-property"></a><span data-ttu-id="c06b4-103">Propriété SoundEffects</span><span class="sxs-lookup"><span data-stu-id="c06b4-103">SoundEffects Property</span></span>

<span data-ttu-id="c06b4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c06b4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c06b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="c06b4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c06b4-106">Retourne une valeur booléenne indiquant si les effets sonores (. WAV) configurés dans le cadre des actions d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="c06b4-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="c06b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="c06b4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c06b4-108">*agent \* \* *. AudioOutput.SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="c06b4-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="c06b4-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="c06b4-109">Value</span></span>     | <span data-ttu-id="c06b4-110">Description</span><span class="sxs-lookup"><span data-stu-id="c06b4-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="c06b4-111">**True**</span><span class="sxs-lookup"><span data-stu-id="c06b4-111">**True**</span></span>  | <span data-ttu-id="c06b4-112">Les effets sonores des caractères sont activés.</span><span class="sxs-lookup"><span data-stu-id="c06b4-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="c06b4-113">**False**</span><span class="sxs-lookup"><span data-stu-id="c06b4-113">**False**</span></span> | <span data-ttu-id="c06b4-114">L’effet sonore des caractères est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c06b4-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c06b4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c06b4-115">Remarks</span></span>

<span data-ttu-id="c06b4-116">Cette propriété reflète l’option lire les effets sonores des caractères sur la page sortie de la feuille de propriétés de l’agent (options des caractères avancés).</span><span class="sxs-lookup"><span data-stu-id="c06b4-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="c06b4-117">Lorsque la propriété **SoundEffects** retourne la **valeur true**, les effets sonores inclus dans la définition d’un caractère sont joués.</span><span class="sxs-lookup"><span data-stu-id="c06b4-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="c06b4-118">Lorsque la **valeur est false**, les effets sonores ne sont pas joués.</span><span class="sxs-lookup"><span data-stu-id="c06b4-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="c06b4-119">Le paramètre de propriété affecte tous les caractères et est en lecture seule ; seul l’utilisateur peut définir cette valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="c06b4-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="c06b4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c06b4-120">See Also</span></span>

[<span data-ttu-id="c06b4-121">**Événement AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="c06b4-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 





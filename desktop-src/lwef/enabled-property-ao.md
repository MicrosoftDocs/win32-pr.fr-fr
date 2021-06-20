---
title: Propriété Enabled (objet AudioOutput)
description: En savoir plus sur la propriété d’objet AudioOutput activée. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407342"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="ed326-104">Propriété Enabled (objet AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="ed326-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="ed326-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed326-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ed326-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="ed326-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ed326-107">Retourne une valeur booléenne indiquant si la sortie audio (parlée) est activée.</span><span class="sxs-lookup"><span data-stu-id="ed326-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="ed326-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="ed326-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ed326-109">*agent \* \* *. AudioOutput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="ed326-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="ed326-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed326-110">Value</span></span>     | <span data-ttu-id="ed326-111">Description</span><span class="sxs-lookup"><span data-stu-id="ed326-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="ed326-112">**True**</span><span class="sxs-lookup"><span data-stu-id="ed326-112">**True**</span></span>  | <span data-ttu-id="ed326-113">Valeurs La sortie audio parlée est activée.</span><span class="sxs-lookup"><span data-stu-id="ed326-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="ed326-114">**False**</span><span class="sxs-lookup"><span data-stu-id="ed326-114">**False**</span></span> | <span data-ttu-id="ed326-115">La sortie audio parlée est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ed326-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed326-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed326-116">Remarks</span></span>

<span data-ttu-id="ed326-117">Cette propriété reflète l’option lire l’audio en sortie dans la page sortie de la feuille de propriétés de l’agent (options des caractères avancés).</span><span class="sxs-lookup"><span data-stu-id="ed326-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="ed326-118">Lorsque la propriété [**Enabled**](enabled-property.md) retourne la **valeur true**, la méthode [**Speak**](speak-method.md) produit une sortie audio si un moteur TTS compatible est installé ou si vous utilisez des fichiers son pour la sortie parlée.</span><span class="sxs-lookup"><span data-stu-id="ed326-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="ed326-119">Quand elle retourne **false**, cela signifie que la sortie vocale n’est pas installée ou a été désactivée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed326-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="ed326-120">Le paramètre de propriété s’applique à tous les caractères de l’agent et est en lecture seule ; seul l’utilisateur peut définir cette valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="ed326-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed326-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed326-121">See Also</span></span>

[<span data-ttu-id="ed326-122">Événement AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="ed326-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 





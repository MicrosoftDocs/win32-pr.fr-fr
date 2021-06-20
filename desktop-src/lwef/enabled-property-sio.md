---
title: Propriété Enabled (objet d’entrée vocale)
description: En savoir plus sur la propriété d’objet d’entrée vocale activée. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: d48f02f1-7d93-4780-88a7-61597672bb58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a3e5d7989da4144805fbb926f744026033638d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407322"
---
# <a name="enabled-property-speech-input-object"></a><span data-ttu-id="0dbb0-104">Propriété Enabled (objet d’entrée vocale)</span><span class="sxs-lookup"><span data-stu-id="0dbb0-104">Enabled Property (Speech Input Object)</span></span>

<span data-ttu-id="0dbb0-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0dbb0-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0dbb0-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="0dbb0-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0dbb0-107">Retourne une valeur booléenne indiquant si l’entrée vocale est activée.</span><span class="sxs-lookup"><span data-stu-id="0dbb0-107">Returns a Boolean value indicating whether speech input is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0dbb0-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="0dbb0-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0dbb0-109">*agent \* \* *. SpeechInput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="0dbb0-109">*agent\*\*\*.SpeechInput.Enabled*\*</span></span>



| <span data-ttu-id="0dbb0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dbb0-110">Value</span></span>     | <span data-ttu-id="0dbb0-111">Description</span><span class="sxs-lookup"><span data-stu-id="0dbb0-111">Description</span></span>               |
|-----------|---------------------------|
| <span data-ttu-id="0dbb0-112">**True**</span><span class="sxs-lookup"><span data-stu-id="0dbb0-112">**True**</span></span>  | <span data-ttu-id="0dbb0-113">L’entrée vocale est activée.</span><span class="sxs-lookup"><span data-stu-id="0dbb0-113">Speech input is enabled.</span></span>  |
| <span data-ttu-id="0dbb0-114">**False**</span><span class="sxs-lookup"><span data-stu-id="0dbb0-114">**False**</span></span> | <span data-ttu-id="0dbb0-115">L’entrée vocale est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0dbb0-115">Speech input is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dbb0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0dbb0-116">Remarks</span></span>

<span data-ttu-id="0dbb0-117">La propriété [**activé**](enabled-property.md) reflète l’option écouter les caractères de l’entrée dans la page entrée vocale de la feuille de propriétés de l’agent (options des caractères avancés).</span><span class="sxs-lookup"><span data-stu-id="0dbb0-117">The [**Enabled**](enabled-property.md) property reflects the Characters Listen For Input option on the Speech Input page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="0dbb0-118">Le paramètre de propriété affecte tous les caractères de l’agent et est en lecture seule ; seul l’utilisateur peut modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0dbb0-118">The property setting affects all Agent characters and is read-only; only the user can change this property.</span></span>

 

 





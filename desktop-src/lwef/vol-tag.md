---
title: Indicateur vol
description: Indicateur vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028764"
---
# <a name="vol-tag"></a><span data-ttu-id="7032a-103">Indicateur vol</span><span class="sxs-lookup"><span data-stu-id="7032a-103">Vol Tag</span></span>

<span data-ttu-id="7032a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7032a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7032a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="7032a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7032a-106">Définit le volume de base de la sortie vocale.</span><span class="sxs-lookup"><span data-stu-id="7032a-106">Sets the baseline speaking volume of the speech output.</span></span>

</dd> <dt>

<span data-ttu-id="7032a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="7032a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7032a-108">**\\Vol =***nombre***\\**</span><span class="sxs-lookup"><span data-stu-id="7032a-108">**\\Vol=***number***\\**</span></span>



| <span data-ttu-id="7032a-109">Partie</span><span class="sxs-lookup"><span data-stu-id="7032a-109">Part</span></span>     | <span data-ttu-id="7032a-110">Description</span><span class="sxs-lookup"><span data-stu-id="7032a-110">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="7032a-111">*number*</span><span class="sxs-lookup"><span data-stu-id="7032a-111">*number*</span></span> | <span data-ttu-id="7032a-112">Volume de base de référence : 0 correspond au silence et 65535 au volume maximal.</span><span class="sxs-lookup"><span data-stu-id="7032a-112">Baseline speaking volume: 0 is silence and 65535 is maximum volume.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="7032a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7032a-113">Remarks</span></span>

<span data-ttu-id="7032a-114">Le paramètre de volume affecte les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="7032a-114">The volume setting affects both left and right channels.</span></span> <span data-ttu-id="7032a-115">Vous ne pouvez pas définir le volume de chaque canal séparément.</span><span class="sxs-lookup"><span data-stu-id="7032a-115">You cannot set the volume of each channel separately.</span></span> <span data-ttu-id="7032a-116">Cette balise est prise en charge uniquement pour la sortie générée par TTS.</span><span class="sxs-lookup"><span data-stu-id="7032a-116">This tag is supported only for TTS-generated output.</span></span>

 

 





---
title: BorderColor, propriété
description: BorderColor, propriété
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981d3ac280669f64219961b74d05c6ba73f1008
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462190"
---
# <a name="bordercolor-property"></a><span data-ttu-id="bb5ae-103">BorderColor, propriété</span><span class="sxs-lookup"><span data-stu-id="bb5ae-103">BorderColor Property</span></span>

<span data-ttu-id="bb5ae-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb5ae-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bb5ae-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="bb5ae-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bb5ae-106">Retourne la couleur de bordure actuellement affichée pour la fenêtre de la bulle du mot pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="bb5ae-106">Returns the border color currently displayed for the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="bb5ae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="bb5ae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bb5ae-108">\* agent ***. Caractères («*** CharacterID \***»).** Balloon. BorderColor</span><span class="sxs-lookup"><span data-stu-id="bb5ae-108">*agent ***.Characters ("*** CharacterID\*\*\*").*\* Balloon.BorderColor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb5ae-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bb5ae-109">Remarks</span></span>

<span data-ttu-id="bb5ae-110">La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="bb5ae-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="bb5ae-111">L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu.</span><span class="sxs-lookup"><span data-stu-id="bb5ae-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="bb5ae-112">Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="bb5ae-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 





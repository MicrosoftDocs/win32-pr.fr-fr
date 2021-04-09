---
title: BackColor, propriété (fonctionnalités de l’environnement Windows hérité)
description: BackColor, propriété
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739653"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a><span data-ttu-id="231a4-103">BackColor, propriété (fonctionnalités de l’environnement Windows hérité)</span><span class="sxs-lookup"><span data-stu-id="231a4-103">BackColor Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="231a4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="231a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="231a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="231a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="231a4-106">Retourne la couleur d’arrière-plan actuellement affichée dans la fenêtre de la bulle du mot pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="231a4-106">Returns the background color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="231a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="231a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="231a4-108">\*agent \***. Caractères («**_CharacterID_*_»). Balloon. BackColor_*</span><span class="sxs-lookup"><span data-stu-id="231a4-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.BackColor_\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="231a4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="231a4-109">Remarks</span></span>

<span data-ttu-id="231a4-110">La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="231a4-110">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="231a4-111">L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu.</span><span class="sxs-lookup"><span data-stu-id="231a4-111">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="231a4-112">Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="231a4-112">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 





---
title: ForeColor, propriété
description: ForeColor, propriété
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839517"
---
# <a name="forecolor-property"></a><span data-ttu-id="8cba7-103">ForeColor, propriété</span><span class="sxs-lookup"><span data-stu-id="8cba7-103">ForeColor Property</span></span>

<span data-ttu-id="8cba7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8cba7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8cba7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8cba7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8cba7-106">Retourne la couleur de premier plan actuellement affichée dans la fenêtre de la bulle du mot pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="8cba7-106">Returns the foreground color currently displayed in the word balloon window for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="8cba7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8cba7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8cba7-108">*agent ***. Caractères («*** CharacterID \* \* * »). Balloon. ForeColor**</span><span class="sxs-lookup"><span data-stu-id="8cba7-108">*agent ***.Characters ("*** CharacterID\*\*\*").Balloon.ForeColor*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cba7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8cba7-109">Remarks</span></span>

<span data-ttu-id="8cba7-110">La propriété **ForeColor** retourne une valeur qui spécifie la couleur du texte dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="8cba7-110">The **ForeColor** property returns a value that specifies the color of text in the word balloon.</span></span> <span data-ttu-id="8cba7-111">La plage valide pour une couleur RVB normale est comprise entre 0 et 16 777 215 (&HFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="8cba7-111">The valid range for a normal RGB color is 0 to 16,777,215 (&HFFFFFF).</span></span> <span data-ttu-id="8cba7-112">L’octet de poids fort d’un nombre de cette plage est égal à 0 ; les 3 octets inférieurs, de l’octet le moins significatif à l’octet le plus significatif, déterminent respectivement la quantité de rouge, de vert et de bleu.</span><span class="sxs-lookup"><span data-stu-id="8cba7-112">The high byte of a number in this range equals 0; the lower 3 bytes, from least to most significant byte, determine the amount of red, green, and blue, respectively.</span></span> <span data-ttu-id="8cba7-113">Chacun des composants rouge, vert et bleu est représenté par un nombre compris entre 0 et 255 (&HFF).</span><span class="sxs-lookup"><span data-stu-id="8cba7-113">The red, green, and blue components are each represented by a number between 0 and 255 (&HFF).</span></span>

 

 





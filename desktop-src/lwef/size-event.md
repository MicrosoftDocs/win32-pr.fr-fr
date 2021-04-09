---
title: Événement de taille
description: Événement de taille
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839866"
---
# <a name="size-event"></a><span data-ttu-id="8806a-103">Événement de taille</span><span class="sxs-lookup"><span data-stu-id="8806a-103">Size Event</span></span>

<span data-ttu-id="8806a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8806a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8806a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8806a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8806a-106">Se produit lorsque la taille d’un caractère change.</span><span class="sxs-lookup"><span data-stu-id="8806a-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="8806a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8806a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8806a-108">Taille du **sous** *-agent* \_ **(ByVal** *CharacterID*, *largeur* **ByVal** , **ByVal** *hauteur*)</span><span class="sxs-lookup"><span data-stu-id="8806a-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="8806a-109">Partie</span><span class="sxs-lookup"><span data-stu-id="8806a-109">Part</span></span>          | <span data-ttu-id="8806a-110">Description</span><span class="sxs-lookup"><span data-stu-id="8806a-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="8806a-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="8806a-111">*CharacterID*</span></span> | <span data-ttu-id="8806a-112">Retourne l’ID du caractère qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="8806a-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="8806a-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="8806a-113">*Width*</span></span>       | <span data-ttu-id="8806a-114">Retourne la nouvelle largeur de la trame de caractère (en pixels) sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="8806a-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="8806a-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="8806a-115">*Height*</span></span>      | <span data-ttu-id="8806a-116">Retourne la nouvelle hauteur de la trame de caractère (en pixels) sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="8806a-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8806a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8806a-117">Remarks</span></span>

<span data-ttu-id="8806a-118">Cet événement se produit lorsqu’une application modifie la taille d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="8806a-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="8806a-119">Cet événement est envoyé uniquement aux clients du caractère (applications qui ont chargé le caractère).</span><span class="sxs-lookup"><span data-stu-id="8806a-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="8806a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8806a-120">See Also</span></span>

[<span data-ttu-id="8806a-121">**Déplacer l’événement**</span><span class="sxs-lookup"><span data-stu-id="8806a-121">**Move event**</span></span>](move-event.md)


 

 





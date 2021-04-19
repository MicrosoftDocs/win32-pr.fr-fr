---
title: Événement Player. KeyPress
description: L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée. | Événement Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Événement KeyPress lecteur Windows Media
- Événement KeyPress lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, KeyPress, événement
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542516"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="03d58-107">Événement Player. KeyPress</span><span class="sxs-lookup"><span data-stu-id="03d58-107">Player.KeyPress event</span></span>

<span data-ttu-id="03d58-108">L’événement **KeyPress** se produit lorsqu’une touche est enfoncée et libérée.</span><span class="sxs-lookup"><span data-stu-id="03d58-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d58-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03d58-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="03d58-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03d58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d58-111">*nKeyAscii*</span><span class="sxs-lookup"><span data-stu-id="03d58-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="03d58-112">**Nombre** (**int**) spécifiant le code ANSI numérique standard pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="03d58-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d58-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03d58-113">Return value</span></span>

<span data-ttu-id="03d58-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03d58-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d58-115">Notes</span><span class="sxs-lookup"><span data-stu-id="03d58-115">Remarks</span></span>

<span data-ttu-id="03d58-116">Cet événement se produit lorsque la séquence de touches génère un caractère imprimable du clavier, la touche CTRL combinée à un caractère de l’alphabet standard ou l’un des quelques caractères spéciaux, et la touche entrée ou retour arrière.</span><span class="sxs-lookup"><span data-stu-id="03d58-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="03d58-117">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="03d58-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="03d58-118">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="03d58-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="03d58-119">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="03d58-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d58-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03d58-120">Requirements</span></span>



| <span data-ttu-id="03d58-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03d58-121">Requirement</span></span> | <span data-ttu-id="03d58-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="03d58-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03d58-123">Version</span><span class="sxs-lookup"><span data-stu-id="03d58-123">Version</span></span><br/> | <span data-ttu-id="03d58-124">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="03d58-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="03d58-125">DLL</span><span class="sxs-lookup"><span data-stu-id="03d58-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="03d58-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d58-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d58-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03d58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d58-128">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="03d58-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 






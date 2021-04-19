---
title: Événement Player. DomainChange
description: L’événement DomainChange se produit lorsque le domaine DVD change. | Événement Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Événement DomainChange lecteur Windows Media
- Événement DomainChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535267"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="449a1-107">Événement Player. DomainChange</span><span class="sxs-lookup"><span data-stu-id="449a1-107">Player.DomainChange event</span></span>

<span data-ttu-id="449a1-108">L’événement **DomainChange** se produit lorsque le domaine DVD change.</span><span class="sxs-lookup"><span data-stu-id="449a1-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="449a1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="449a1-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="449a1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="449a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="449a1-111">*strDomain*</span><span class="sxs-lookup"><span data-stu-id="449a1-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="449a1-112">**Chaîne** indiquant le nouveau domaine.</span><span class="sxs-lookup"><span data-stu-id="449a1-112">**String** indicating the new domain.</span></span> <span data-ttu-id="449a1-113">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="449a1-113">Contains one of the following values.</span></span>



| <span data-ttu-id="449a1-114">String</span><span class="sxs-lookup"><span data-stu-id="449a1-114">String</span></span>            | <span data-ttu-id="449a1-115">Description</span><span class="sxs-lookup"><span data-stu-id="449a1-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="449a1-116">firstplay</span><span class="sxs-lookup"><span data-stu-id="449a1-116">firstplay</span></span>         | <span data-ttu-id="449a1-117">Exécution de l’initialisation par défaut d’un disque DVD.</span><span class="sxs-lookup"><span data-stu-id="449a1-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="449a1-118">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="449a1-118">videoManagerMenu</span></span>  | <span data-ttu-id="449a1-119">Affichage des menus pour la totalité du disque. Également appelé menu racine ou menu principal.</span><span class="sxs-lookup"><span data-stu-id="449a1-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="449a1-120">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="449a1-120">videoTitleSetMenu</span></span> | <span data-ttu-id="449a1-121">Affichage des menus pour le jeu de titres actuel.</span><span class="sxs-lookup"><span data-stu-id="449a1-121">Displaying menus for current title set.</span></span> <span data-ttu-id="449a1-122">Également appelé titleMenu.</span><span class="sxs-lookup"><span data-stu-id="449a1-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="449a1-123">title</span><span class="sxs-lookup"><span data-stu-id="449a1-123">title</span></span>             | <span data-ttu-id="449a1-124">Affichage du titre actuel.</span><span class="sxs-lookup"><span data-stu-id="449a1-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="449a1-125">stop</span><span class="sxs-lookup"><span data-stu-id="449a1-125">stop</span></span>              | <span data-ttu-id="449a1-126">Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.</span><span class="sxs-lookup"><span data-stu-id="449a1-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="449a1-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="449a1-127">Return value</span></span>

<span data-ttu-id="449a1-128">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="449a1-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="449a1-129">Notes</span><span class="sxs-lookup"><span data-stu-id="449a1-129">Remarks</span></span>

<span data-ttu-id="449a1-130">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="449a1-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="449a1-131">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="449a1-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="449a1-132">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="449a1-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="449a1-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="449a1-133">Requirements</span></span>



| <span data-ttu-id="449a1-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="449a1-134">Requirement</span></span> | <span data-ttu-id="449a1-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="449a1-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="449a1-136">Version</span><span class="sxs-lookup"><span data-stu-id="449a1-136">Version</span></span><br/> | <span data-ttu-id="449a1-137">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="449a1-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="449a1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="449a1-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="449a1-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="449a1-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="449a1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="449a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449a1-141">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="449a1-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="449a1-142">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="449a1-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 






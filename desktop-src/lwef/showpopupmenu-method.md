---
title: Méthode ShowPopupMenu
description: Méthode ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533298"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="f555b-103">Méthode ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="f555b-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="f555b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f555b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f555b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f555b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f555b-106">Affiche le menu contextuel du caractère à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="f555b-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="f555b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f555b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f555b-108">*agent. ***Caractères («*** CharacterID ***»). ShowPopupMenu*** x, y*</span><span class="sxs-lookup"><span data-stu-id="f555b-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="f555b-109">Partie</span><span class="sxs-lookup"><span data-stu-id="f555b-109">Part</span></span> | <span data-ttu-id="f555b-110">Description</span><span class="sxs-lookup"><span data-stu-id="f555b-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f555b-111">*x*</span><span class="sxs-lookup"><span data-stu-id="f555b-111">*x*</span></span>  | <span data-ttu-id="f555b-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f555b-112">Required.</span></span> <span data-ttu-id="f555b-113">Valeur entière qui indique la coordonnée d’écran horizontale (*x*) pour afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="f555b-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="f555b-114">Ces coordonnées doivent être spécifiées en pixels.</span><span class="sxs-lookup"><span data-stu-id="f555b-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="f555b-115">*y*</span><span class="sxs-lookup"><span data-stu-id="f555b-115">*y*</span></span>  | <span data-ttu-id="f555b-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f555b-116">Required.</span></span> <span data-ttu-id="f555b-117">Valeur entière qui indique la coordonnée d’écran verticale (*y*) pour afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="f555b-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="f555b-118">Ces coordonnées doivent être spécifiées en pixels.</span><span class="sxs-lookup"><span data-stu-id="f555b-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f555b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f555b-119">Remarks</span></span>

<span data-ttu-id="f555b-120">Agent affiche automatiquement le menu contextuel du caractère lorsque l’utilisateur clique avec le bouton droit sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="f555b-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="f555b-121">Si vous affectez à [**AutoPopupMenu**](autopopupmenu-property.md) la **valeur false**, vous pouvez utiliser cette méthode pour afficher le menu.</span><span class="sxs-lookup"><span data-stu-id="f555b-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="f555b-122">Le menu reste affiché jusqu’à ce que l’utilisateur sélectionne une commande ou affiche un autre menu.</span><span class="sxs-lookup"><span data-stu-id="f555b-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="f555b-123">Un seul menu contextuel peut être affiché à la fois ; par conséquent, les appels à cette méthode annulent (supprime) le menu précédent.</span><span class="sxs-lookup"><span data-stu-id="f555b-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="f555b-124">Cette méthode doit être appelée uniquement lorsque votre application cliente est le client actif du caractère ; dans le cas contraire, elle échoue.</span><span class="sxs-lookup"><span data-stu-id="f555b-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="f555b-125">Pour déterminer la réussite de cette méthode, vous pouvez l’appeler en tant que fonction et retourner une valeur booléenne indiquant si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f555b-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="f555b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f555b-126">See Also</span></span>

[<span data-ttu-id="f555b-127">**Propriété AutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="f555b-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 





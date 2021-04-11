---
title: Propriété AutoPopupMenu
description: Propriété AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310806"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="f6ba7-103">Propriété AutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="f6ba7-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="f6ba7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6ba7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f6ba7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f6ba7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f6ba7-106">Retourne ou définit une valeur indiquant si le fait de cliquer avec le bouton droit sur le caractère ou l’icône de la barre des tâches affiche automatiquement le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f6ba7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f6ba7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f6ba7-108">\*agent. ***Caractères \* \* \* \* ("*** CharacterID \* \* *"). AutoPopupMenu* \*  \[  =  *booléen*\]</span><span class="sxs-lookup"><span data-stu-id="f6ba7-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="f6ba7-109">Partie</span><span class="sxs-lookup"><span data-stu-id="f6ba7-109">Part</span></span>      | <span data-ttu-id="f6ba7-110">Description</span><span class="sxs-lookup"><span data-stu-id="f6ba7-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ba7-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="f6ba7-111">*boolean*</span></span> | <span data-ttu-id="f6ba7-112">Expression booléenne spécifiant si le serveur affiche automatiquement le menu contextuel du caractère en cliquant dessus avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="f6ba7-113">**True** (par défaut) affiche le menu en cliquant avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="f6ba7-114">**Valeur false** N’affiche pas le menu en cliquant avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6ba7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f6ba7-115">Remarks</span></span>

<span data-ttu-id="f6ba7-116">En affectant à cette propriété la **valeur false**, vous pouvez créer votre propre comportement de gestion de menus.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="f6ba7-117">Pour afficher le menu après avoir défini cette propriété sur **false**, utilisez la méthode [**ShowPopupMenu**](showpopupmenu-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f6ba7-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="f6ba7-118">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="f6ba7-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6ba7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6ba7-119">See Also</span></span>

[<span data-ttu-id="f6ba7-120">**Méthode ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="f6ba7-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 






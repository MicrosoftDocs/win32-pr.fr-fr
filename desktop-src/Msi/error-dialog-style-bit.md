---
description: Si ce bit est défini, la boîte de dialogue est une boîte de dialogue d’erreur.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit de style de boîte de dialogue d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519354"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="b8fc9-103">Bit de style de boîte de dialogue d’erreur</span><span class="sxs-lookup"><span data-stu-id="b8fc9-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="b8fc9-104">Si ce bit est défini, la boîte de dialogue est une boîte de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="b8fc9-105">Il peut y avoir plusieurs boîtes de dialogue avec ce style.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="b8fc9-106">La propriété **ErrorDialog** détermine la boîte de dialogue qui est utilisée comme boîte de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="b8fc9-107">La boîte de dialogue sélectionnée peut être une seule de celles pour lesquelles ce bit de style est défini.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="b8fc9-108">La boîte de dialogue d’erreur doit avoir un contrôle de texte statique nommé ErrorText.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="b8fc9-109">Ce contrôle reçoit le texte du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-109">This control receives the text of the error message.</span></span> <span data-ttu-id="b8fc9-110">La boîte de dialogue doit également comporter les sept boutons de commande correspondant aux valeurs de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="b8fc9-111">Le message d’erreur détermine lequel de ces boutons est réellement affiché.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="b8fc9-112">Les boutons affichés sont réorganisés de sorte qu’ils sont répartis uniformément dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="b8fc9-113">Cette réorganisation modifie la coordonnée X des boutons, mais pas les trois autres coordonnées.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="b8fc9-114">Par conséquent, il est recommandé qu’aucun autre contrôle ne soit créé dans la même région horizontale de la boîte de dialogue que les boutons.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="b8fc9-115">Si le message d’erreur ne spécifie aucun bouton, le bouton **OK** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="b8fc9-116">Le bouton **par défaut** , le premier contrôle actif et les valeurs du bouton **Annuler** sont ignorés pour une boîte de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="b8fc9-117">Le bouton **par défaut** défini dans le message d’erreur sera affecté aux trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="b8fc9-118">L’effet de l’exécution de ces boutons doit être défini dans la [table ControlEvent,](controlevent-table.md) comme pour tous les autres boutons.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="b8fc9-119">Le titre de la boîte de dialogue est créé d’une manière similaire à d’autres boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="b8fc9-120">Il peut être remplacé par le message d’erreur s’il spécifie un texte d’en-tête après la liste de boutons.</span><span class="sxs-lookup"><span data-stu-id="b8fc9-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="b8fc9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8fc9-121">Value</span></span>



| <span data-ttu-id="b8fc9-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="b8fc9-122">Decimal</span></span> | <span data-ttu-id="b8fc9-123">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="b8fc9-123">Hexadecimal</span></span> | <span data-ttu-id="b8fc9-124">Constante</span><span class="sxs-lookup"><span data-stu-id="b8fc9-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="b8fc9-125">65536</span><span class="sxs-lookup"><span data-stu-id="b8fc9-125">65536</span></span>   | <span data-ttu-id="b8fc9-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b8fc9-126">0x00010000</span></span>  | <span data-ttu-id="b8fc9-127">**msidbDialogAttributesError**</span><span class="sxs-lookup"><span data-stu-id="b8fc9-127">**msidbDialogAttributesError**</span></span> |



 

 

 




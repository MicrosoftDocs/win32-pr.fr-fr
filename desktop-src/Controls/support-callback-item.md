---
title: Comment prendre en charge les éléments de rappel
description: Cette rubrique montre comment assurer la prise en charge des éléments de rappel.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941478"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="0f2ff-103">Comment prendre en charge les éléments de rappel</span><span class="sxs-lookup"><span data-stu-id="0f2ff-103">How to Support Callback Items</span></span>

<span data-ttu-id="0f2ff-104">Cette rubrique montre comment assurer la prise en charge des éléments de rappel.</span><span class="sxs-lookup"><span data-stu-id="0f2ff-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0f2ff-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="0f2ff-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0f2ff-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="0f2ff-106">Technologies</span></span>

-   [<span data-ttu-id="0f2ff-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="0f2ff-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0f2ff-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0f2ff-108">Prerequisites</span></span>

-   <span data-ttu-id="0f2ff-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="0f2ff-109">C/C++</span></span>
-   <span data-ttu-id="0f2ff-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="0f2ff-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0f2ff-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="0f2ff-111">Instructions</span></span>


<span data-ttu-id="0f2ff-112">Si votre application va utiliser des éléments de rappel dans un contrôle ComboBoxEx, elle doit être préparée à gérer le code de notification [CBEN \_ GETDISPINFO](cben-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0f2ff-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="0f2ff-113">Un contrôle ComboBoxEx envoie cette notification chaque fois qu’il a besoin du propriétaire pour fournir des informations spécifiques sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="0f2ff-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="0f2ff-114">Pour plus d’informations sur les éléments de rappel, consultez [éléments de rappel](comboboxex-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0f2ff-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="0f2ff-115">La fonction suivante définie par l’application traite [CBEN \_ GETDISPINFO](cben-getdispinfo.md) en fournissant des attributs pour un élément donné.</span><span class="sxs-lookup"><span data-stu-id="0f2ff-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="0f2ff-116">Notez qu’elle définit le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) entrante sur CBEIF \_ di \_ SETITEM.</span><span class="sxs-lookup"><span data-stu-id="0f2ff-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="0f2ff-117">Si vous définissez le **masque** sur cette valeur, le contrôle conserve les informations de l’élément afin qu’il n’ait pas besoin de demander à nouveau les informations.</span><span class="sxs-lookup"><span data-stu-id="0f2ff-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="0f2ff-118">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="0f2ff-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="0f2ff-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f2ff-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2ff-120">À propos des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0f2ff-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="0f2ff-121">Référence du contrôle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0f2ff-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0f2ff-122">Utilisation des contrôles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0f2ff-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="0f2ff-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="0f2ff-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 
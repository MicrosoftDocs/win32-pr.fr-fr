---
title: Curseurs (Windows Multimedia)
description: Curseurs
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixages audio, contrôles
- mixages audio, curseurs
- mélangeurs, contrôles
- mélangeurs, curseurs
- contrôles Slider
- Structure MIXERCONTROLDETAILS_SIGNED
- contrôle panoramique
- Contrôle PAN QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383631"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="be406-111">Curseurs (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="be406-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="be406-112">Les contrôles Slider sont généralement des contrôles horizontaux qui peuvent être ajustés à gauche ou à droite.</span><span class="sxs-lookup"><span data-stu-id="be406-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="be406-113">Ces contrôles utilisent la [**structure \_ signée MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) pour récupérer et définir des propriétés de contrôle.</span><span class="sxs-lookup"><span data-stu-id="be406-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="be406-114">Le tableau suivant décrit les types de curseurs.</span><span class="sxs-lookup"><span data-stu-id="be406-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="be406-115">Contrôler</span><span class="sxs-lookup"><span data-stu-id="be406-115">Control</span></span>    | <span data-ttu-id="be406-116">Description</span><span class="sxs-lookup"><span data-stu-id="be406-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be406-117">Curseur</span><span class="sxs-lookup"><span data-stu-id="be406-117">Slider</span></span>     | <span data-ttu-id="be406-118">A une plage comprise entre – 32 768 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="be406-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="be406-119">Le pilote de mixage définit les limites de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="be406-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="be406-120">Panoramique</span><span class="sxs-lookup"><span data-stu-id="be406-120">Pan</span></span>        | <span data-ttu-id="be406-121">A une plage comprise entre – 32 768 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="be406-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="be406-122">Le pilote de mixage définit les limites de ce contrôle, 0 étant la valeur de milieu de gamme.</span><span class="sxs-lookup"><span data-stu-id="be406-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="be406-123">Panoramique QSound</span><span class="sxs-lookup"><span data-stu-id="be406-123">QSound Pan</span></span> | <span data-ttu-id="be406-124">Fournit un contrôle du son développé via QSound.</span><span class="sxs-lookup"><span data-stu-id="be406-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="be406-125">Ce contrôle a une plage comprise entre – 15 et 15.</span><span class="sxs-lookup"><span data-stu-id="be406-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 

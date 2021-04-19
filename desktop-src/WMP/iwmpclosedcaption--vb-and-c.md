---
title: Interface IWMPClosedCaption (VB et C) (WMP. h)
description: Offre un moyen d’inclure des sous-titres avec un fichier multimédia numérique. Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- IWMPClosedCaption (VB et C) interface Windows Media Player
- Interface IWMPClosedCaption (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525259"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="43082-106">Interface IWMPClosedCaption (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="43082-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="43082-107">Offre un moyen d’inclure des sous-titres avec un fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="43082-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="43082-108">Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="43082-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="43082-109">Membres</span><span class="sxs-lookup"><span data-stu-id="43082-109">Members</span></span>

<span data-ttu-id="43082-110">L’interface **IWMPClosedCaption (VB et C#)** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="43082-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="43082-111">L’interface **IWMPClosedCaption** expose les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="43082-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="43082-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="43082-112">Property</span></span>                                                                             | <span data-ttu-id="43082-113">Description</span><span class="sxs-lookup"><span data-stu-id="43082-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43082-114">captioningId</span><span class="sxs-lookup"><span data-stu-id="43082-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="43082-115">Obtient ou définit le nom de l’élément HTML affichant le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="43082-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="43082-116">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="43082-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="43082-117">Obtient ou définit le nom du fichier contenant les informations nécessaires pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="43082-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="43082-118">SAMILang</span><span class="sxs-lookup"><span data-stu-id="43082-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="43082-119">Obtient ou définit la langue affichée pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="43082-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="43082-120">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="43082-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="43082-121">Obtient ou définit le style de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="43082-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="43082-122">Procurez-vous une interface **IWMPClosedCaption** à l’aide de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="43082-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="43082-123">Object</span><span class="sxs-lookup"><span data-stu-id="43082-123">Object</span></span>                                                            | <span data-ttu-id="43082-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="43082-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="43082-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="43082-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="43082-126">closedCaption</span><span class="sxs-lookup"><span data-stu-id="43082-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="43082-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43082-127">Requirements</span></span>



| <span data-ttu-id="43082-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43082-128">Requirement</span></span> | <span data-ttu-id="43082-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="43082-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="43082-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="43082-130">Header</span></span><br/> | <dl> <span data-ttu-id="43082-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="43082-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43082-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43082-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43082-133">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="43082-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="43082-134">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="43082-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="43082-135">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="43082-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






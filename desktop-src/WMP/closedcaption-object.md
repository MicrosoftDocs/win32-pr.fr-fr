---
title: Objet ClosedCaption
description: L’objet ClosedCaption offre un moyen d’inclure des sous-titres avec un clip multimédia. Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Objet ClosedCaption lecteur Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030455"
---
# <a name="closedcaption-object"></a><span data-ttu-id="6d52c-105">Objet ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="6d52c-105">ClosedCaption Object</span></span>

<span data-ttu-id="6d52c-106">L’objet **ClosedCaption** offre un moyen d’inclure des sous-titres avec un clip multimédia.</span><span class="sxs-lookup"><span data-stu-id="6d52c-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="6d52c-107">Le texte de sous-titrage se trouve dans un fichier SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="6d52c-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="6d52c-108">L’objet **ClosedCaption** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d52c-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="6d52c-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="6d52c-109">Property</span></span>                                           | <span data-ttu-id="6d52c-110">Description</span><span class="sxs-lookup"><span data-stu-id="6d52c-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d52c-111">captioningID</span><span class="sxs-lookup"><span data-stu-id="6d52c-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="6d52c-112">Spécifie ou récupère le nom du frame ou du contrôle qui affiche le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="6d52c-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="6d52c-113">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="6d52c-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="6d52c-114">Spécifie ou récupère le nom du fichier contenant les informations nécessaires pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="6d52c-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="6d52c-115">SAMILang</span><span class="sxs-lookup"><span data-stu-id="6d52c-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="6d52c-116">Spécifie ou récupère la langue affichée pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="6d52c-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="6d52c-117">SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="6d52c-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="6d52c-118">Récupère le nombre de langues prises en charge par le fichier SAMI actuel.</span><span class="sxs-lookup"><span data-stu-id="6d52c-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="6d52c-119">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="6d52c-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="6d52c-120">Spécifie ou récupère le style de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="6d52c-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="6d52c-121">SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="6d52c-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="6d52c-122">Récupère le nombre de styles pris en charge par le fichier SAMI actuel.</span><span class="sxs-lookup"><span data-stu-id="6d52c-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="6d52c-123">L’objet **ClosedCaption** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6d52c-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="6d52c-124">Méthode</span><span class="sxs-lookup"><span data-stu-id="6d52c-124">Method</span></span>                                                 | <span data-ttu-id="6d52c-125">Description</span><span class="sxs-lookup"><span data-stu-id="6d52c-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d52c-126">getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="6d52c-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="6d52c-127">Récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.</span><span class="sxs-lookup"><span data-stu-id="6d52c-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="6d52c-128">getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="6d52c-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="6d52c-129">Récupère le nom d’une langue prise en charge par le fichier SAMI actuel.</span><span class="sxs-lookup"><span data-stu-id="6d52c-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="6d52c-130">getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="6d52c-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="6d52c-131">Récupère le nom d’un style pris en charge par le fichier SAMI actuel.</span><span class="sxs-lookup"><span data-stu-id="6d52c-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="6d52c-132">L’objet **ClosedCaption** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="6d52c-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="6d52c-133">Object</span><span class="sxs-lookup"><span data-stu-id="6d52c-133">Object</span></span>                      | <span data-ttu-id="6d52c-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="6d52c-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="6d52c-135">Lecteur</span><span class="sxs-lookup"><span data-stu-id="6d52c-135">Player</span></span>](player-object.md) | [<span data-ttu-id="6d52c-136">closedCaption</span><span class="sxs-lookup"><span data-stu-id="6d52c-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="6d52c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d52c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d52c-138">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="6d52c-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6d52c-139">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="6d52c-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





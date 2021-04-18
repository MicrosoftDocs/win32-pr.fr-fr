---
title: STARTTIME, élément
description: L’élément STARTTIME définit un index de temps à partir duquel le lecteur Windows Media va commencer le rendu du flux.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME, élément Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526023"
---
# <a name="starttime-element"></a><span data-ttu-id="52b18-104">STARTTIME, élément</span><span class="sxs-lookup"><span data-stu-id="52b18-104">STARTTIME Element</span></span>

<span data-ttu-id="52b18-105">L’élément **StartTime** définit un index de temps à partir duquel le lecteur Windows Media va commencer le rendu du flux.</span><span class="sxs-lookup"><span data-stu-id="52b18-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="52b18-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="52b18-106">Attributes</span></span>

<span data-ttu-id="52b18-107">**Valeur** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="52b18-107">**VALUE** (required)</span></span>

<span data-ttu-id="52b18-108">L’index de temps (en heures, minutes, secondes et centièmes de seconde) à partir duquel le lecteur Windows Media commence à lire un flux défini dans l’élément associé.</span><span class="sxs-lookup"><span data-stu-id="52b18-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="52b18-109">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="52b18-109">Parent/Child Elements</span></span>



| <span data-ttu-id="52b18-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="52b18-110">Hierarchy</span></span>       | <span data-ttu-id="52b18-111">Éléments</span><span class="sxs-lookup"><span data-stu-id="52b18-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="52b18-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52b18-112">Parent elements</span></span> | <span data-ttu-id="52b18-113">**entry**, **ref**</span><span class="sxs-lookup"><span data-stu-id="52b18-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="52b18-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52b18-114">Child elements</span></span>  | <span data-ttu-id="52b18-115">Aucune</span><span class="sxs-lookup"><span data-stu-id="52b18-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="52b18-116">Notes</span><span class="sxs-lookup"><span data-stu-id="52b18-116">Remarks</span></span>

<span data-ttu-id="52b18-117">Cet élément définit un index de temps dans le contenu où le lecteur Windows Media doit commencer le rendu du flux.</span><span class="sxs-lookup"><span data-stu-id="52b18-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="52b18-118">Cet élément peut être utilisé uniquement avec le contenu stocké à la demande qui a été indexé.</span><span class="sxs-lookup"><span data-stu-id="52b18-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="52b18-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="52b18-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="52b18-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52b18-120">Requirements</span></span>



| <span data-ttu-id="52b18-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52b18-121">Requirement</span></span> | <span data-ttu-id="52b18-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="52b18-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="52b18-123">Version</span><span class="sxs-lookup"><span data-stu-id="52b18-123">Version</span></span><br/> | <span data-ttu-id="52b18-124">Lecteur Windows Media version 70 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="52b18-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52b18-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52b18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b18-126">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="52b18-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="52b18-127">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="52b18-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






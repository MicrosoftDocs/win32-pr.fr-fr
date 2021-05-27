---
title: Échec du dessin D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Échec d’un appel de dessin par une cible de rendu
keywords:
- Erreur de dessin D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549964"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="b04ed-104">D1109 : échec du dessin</span><span class="sxs-lookup"><span data-stu-id="b04ed-104">D1109: Draw Failure</span></span>

<span data-ttu-id="b04ed-105">Un appel de dessin par une cible de rendu a échoué \[  \] .</span><span class="sxs-lookup"><span data-stu-id="b04ed-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="b04ed-106">Balises \[ *: étiquette1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="b04ed-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="b04ed-107">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="b04ed-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b04ed-108"><span id="resource"></span><span id="RESOURCE"></span>*ressource*</span><span class="sxs-lookup"><span data-stu-id="b04ed-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="b04ed-109">Adresse de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b04ed-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="b04ed-110"><span id="tag1"></span><span id="TAG1"></span>*: étiquette1*</span><span class="sxs-lookup"><span data-stu-id="b04ed-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="b04ed-111">La première valeur de la balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="b04ed-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="b04ed-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="b04ed-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="b04ed-113">La deuxième valeur de balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="b04ed-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="b04ed-114">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="b04ed-114">Error Level</span></span> | <span data-ttu-id="b04ed-115">Avertissement</span><span class="sxs-lookup"><span data-stu-id="b04ed-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="b04ed-116">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="b04ed-116">Possible Causes</span></span>

<span data-ttu-id="b04ed-117">Un appel de dessin peut échouer pour de nombreuses raisons.</span><span class="sxs-lookup"><span data-stu-id="b04ed-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="b04ed-118">Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Direct2D pour la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="b04ed-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 
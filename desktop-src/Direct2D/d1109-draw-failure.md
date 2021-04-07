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
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730077"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="70c95-104">D1109 : échec du dessin</span><span class="sxs-lookup"><span data-stu-id="70c95-104">D1109: Draw Failure</span></span>

<span data-ttu-id="70c95-105">Un appel de dessin par une cible de rendu a échoué \[  \] .</span><span class="sxs-lookup"><span data-stu-id="70c95-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="70c95-106">Balises \[ *: étiquette1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="70c95-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="70c95-107">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="70c95-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="70c95-108"><span id="resource"></span><span id="RESOURCE"></span>*ressource*</span><span class="sxs-lookup"><span data-stu-id="70c95-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="70c95-109">Adresse de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="70c95-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="70c95-110"><span id="tag1"></span><span id="TAG1"></span>*: étiquette1*</span><span class="sxs-lookup"><span data-stu-id="70c95-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="70c95-111">La première valeur de la balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="70c95-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="70c95-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="70c95-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="70c95-113">La deuxième valeur de balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).</span><span class="sxs-lookup"><span data-stu-id="70c95-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="70c95-114">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="70c95-114">Error Level</span></span> | <span data-ttu-id="70c95-115">Avertissement</span><span class="sxs-lookup"><span data-stu-id="70c95-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="70c95-116">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="70c95-116">Possible Causes</span></span>

<span data-ttu-id="70c95-117">Un appel de dessin peut échouer pour de nombreuses raisons.</span><span class="sxs-lookup"><span data-stu-id="70c95-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="70c95-118">Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Direct2D pour la méthode qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="70c95-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 
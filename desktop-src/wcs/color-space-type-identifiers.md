---
title: Identificateurs de types d’espace de couleurs
description: Ces constantes spécifient le type d’un tableau d’espace colorimétrique PostScript 2. Les valeurs suivantes sont des types de tableau d’espace colorimétrique valides.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "106535728"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="bf94f-104">Identificateurs de types d’espace de couleurs</span><span class="sxs-lookup"><span data-stu-id="bf94f-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="bf94f-105">Ces constantes spécifient le type d’un tableau d’espace colorimétrique PostScript 2.</span><span class="sxs-lookup"><span data-stu-id="bf94f-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="bf94f-106">Les valeurs suivantes sont des types de tableau d’espace colorimétrique valides.</span><span class="sxs-lookup"><span data-stu-id="bf94f-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="bf94f-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="bf94f-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-108">Obtenir un tableau d’espace colorimétrique CIEBasedA à partir du profil monochrome.</span><span class="sxs-lookup"><span data-stu-id="bf94f-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_gris CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-110">Obtenir un tableau d’espace colorimétrique CIEBasedA à partir du profil monochrome.</span><span class="sxs-lookup"><span data-stu-id="bf94f-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_**</span><span class="sxs-lookup"><span data-stu-id="bf94f-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-112">Obtenir un tableau d’espace de couleurs CIEBasedABC à partir du profil RVB ou L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bf94f-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**\_définition CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-114">Obtenir un tableau d’espace de couleurs CIEBasedDEF à partir du profil RVB ou L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bf94f-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**\_RGB CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-116">Obtenir un tableau d’espace de couleurs CIEBasedDEF suivi d’un tableau d’espaces de couleurs CIEBasedABC à partir du profil RGB.</span><span class="sxs-lookup"><span data-stu-id="bf94f-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="bf94f-117">À l’exécution, si l’imprimante ne prend pas en charge les espaces de couleurs CIEBasedDEF, la fonction utilise la définition CIEBasedABC.</span><span class="sxs-lookup"><span data-stu-id="bf94f-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratoire CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-119">Obtient un tableau d’espaces de couleurs CIEBasedABC à partir du <sup>\*</sup> Profil L a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bf94f-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_DEFG CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-121">Obtenir un tableau d’espace colorimétrique CIEBasedDEFG à partir du profil CMJN.</span><span class="sxs-lookup"><span data-stu-id="bf94f-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf94f-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**\_CMJN CSA**</span><span class="sxs-lookup"><span data-stu-id="bf94f-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bf94f-123">Obtenir un tableau d’espace colorimétrique CIEBasedCMYK à partir du profil CMJN.</span><span class="sxs-lookup"><span data-stu-id="bf94f-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bf94f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf94f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf94f-125">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="bf94f-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="bf94f-126">Constantes ICM</span><span class="sxs-lookup"><span data-stu-id="bf94f-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 





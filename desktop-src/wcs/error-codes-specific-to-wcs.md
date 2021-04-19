---
title: Codes d’erreur spécifiques du WCS
description: La liste suivante répertorie les codes d’erreur qui sont spécifiquement liés à l’utilisation du WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "106522260"
---
# <a name="error-codes-specific-to-wcs"></a><span data-ttu-id="19a81-103">Codes d’erreur spécifiques du WCS</span><span class="sxs-lookup"><span data-stu-id="19a81-103">Error Codes Specific To WCS</span></span>

<span data-ttu-id="19a81-104">La liste suivante répertorie les codes d’erreur qui sont spécifiquement liés à l’utilisation du WCS 1,0.</span><span class="sxs-lookup"><span data-stu-id="19a81-104">The following is a list of error codes that are specifically related to the use of WCS 1.0.</span></span> <span data-ttu-id="19a81-105">Cela ne signifie pas que les fonctions WCS ne retournent que ces codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="19a81-105">This does not mean that WCS functions will return only these error codes.</span></span> <span data-ttu-id="19a81-106">Cela signifie que les codes du tableau ci-dessous sont retournés uniquement par les fonctions WCS.</span><span class="sxs-lookup"><span data-stu-id="19a81-106">It means that the codes in the table below are returned only by WCS functions.</span></span> <span data-ttu-id="19a81-107">Ils peuvent également retourner d’autres codes d’erreur Win32 documentés ailleurs dans l’API Win32 du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="19a81-107">They may also return other Win32 error codes that are documented elsewhere in the Win32 API of the Platform SDK.</span></span>

<dl> <dt>

<span data-ttu-id="19a81-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERREUR lors de \_ la suppression du \_ \_ XForm CCI</span><span class="sxs-lookup"><span data-stu-id="19a81-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR\_DELETING\_ICM\_XFORM</span></span>
</dt> <dd>

<span data-ttu-id="19a81-109">La transformation de couleur spécifiée n’a pas pu être supprimée.</span><span class="sxs-lookup"><span data-stu-id="19a81-109">The specified color transform could not be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>\_balise d’erreur dupliquée \_</span><span class="sxs-lookup"><span data-stu-id="19a81-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR\_DUPLICATE\_TAG</span></span>
</dt> <dd>

<span data-ttu-id="19a81-111">La balise d’élément de profil de couleurs spécifiée est déjà présente dans le profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="19a81-111">The specified color profile element tag is already present in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERREUR \_ ICM \_ non \_ activée</span><span class="sxs-lookup"><span data-stu-id="19a81-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR\_ICM\_NOT\_ENABLED</span></span>
</dt> <dd>

<span data-ttu-id="19a81-113">La gestion des couleurs des images n’est pas activée actuellement.</span><span class="sxs-lookup"><span data-stu-id="19a81-113">Image Color Management is not currently enabled.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERREUR \_ CMM non valide \_</span><span class="sxs-lookup"><span data-stu-id="19a81-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR\_INVALID\_CMM</span></span>
</dt> <dd>

<span data-ttu-id="19a81-115">Le nom de fichier spécifié ne fait pas référence à un module de gestion de couleurs valide.</span><span class="sxs-lookup"><span data-stu-id="19a81-115">The specified file name does not refer to a valid color management module.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERREUR \_ COLORSPACE non valide \_</span><span class="sxs-lookup"><span data-stu-id="19a81-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR\_INVALID\_COLORSPACE</span></span>
</dt> <dd>

<span data-ttu-id="19a81-117">L’espace de couleurs spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="19a81-117">The specified color space is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERREUR \_ de \_ Profil non valide</span><span class="sxs-lookup"><span data-stu-id="19a81-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR\_INVALID\_PROFILE</span></span>
</dt> <dd>

<span data-ttu-id="19a81-119">Le nom de fichier spécifié ne fait pas référence à un profil de couleurs valide.</span><span class="sxs-lookup"><span data-stu-id="19a81-119">The specified file name does not refer to a valid color profile.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERREUR \_ de \_ transformation non valide</span><span class="sxs-lookup"><span data-stu-id="19a81-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR\_INVALID\_TRANSFORM</span></span> 
</dt> <dd>

<span data-ttu-id="19a81-121">La transformation de couleur qui a été spécifiée n’est pas une transformation de couleur valide.</span><span class="sxs-lookup"><span data-stu-id="19a81-121">The color transform that was specified is not a valid color transform.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_profil \_ d’erreur non \_ associé à l' \_ \_ appareil</span><span class="sxs-lookup"><span data-stu-id="19a81-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="19a81-123">Le profil de couleurs spécifié n’est associé à aucun appareil.</span><span class="sxs-lookup"><span data-stu-id="19a81-123">The specified color profile is not associated with any device.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_profil d' \_ erreur \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="19a81-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>ERROR\_PROFILE\_NOT\_FOUND</span></span> 
</dt> <dd>

<span data-ttu-id="19a81-125">Le nom de fichier du profil de couleurs spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="19a81-125">The specified color profile file name was not found.</span></span> <span data-ttu-id="19a81-126">Le nom ou le chemin d’accès du fichier est incorrect.</span><span class="sxs-lookup"><span data-stu-id="19a81-126">The file name or path is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_balise d’erreur \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="19a81-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>ERROR\_TAG\_NOT\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="19a81-128">La balise d’élément de profil de couleur spécifiée est introuvable dans le profil de couleurs.</span><span class="sxs-lookup"><span data-stu-id="19a81-128">The specified color profile element tag was not found in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="19a81-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>\_balise d’erreur \_ \_ absente</span><span class="sxs-lookup"><span data-stu-id="19a81-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>ERROR\_TAG\_NOT\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="19a81-130">Une balise d’élément de profil de couleur requise pour que la fonction aboutisse n’a pas été passée à la fonction.</span><span class="sxs-lookup"><span data-stu-id="19a81-130">A color profile element tag that is required for the function to succeed was not passed to the function.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="19a81-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19a81-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a81-132">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="19a81-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="19a81-133">Constantes WCS</span><span class="sxs-lookup"><span data-stu-id="19a81-133">WCS Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 





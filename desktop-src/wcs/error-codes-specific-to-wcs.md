---
title: Codes d’erreur spécifiques du WCS
description: La liste suivante répertorie les codes d’erreur qui sont spécifiquement liés à l’utilisation du WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814599"
---
# <a name="error-codes-specific-to-wcs"></a>Codes d’erreur spécifiques du WCS

La liste suivante répertorie les codes d’erreur qui sont spécifiquement liés à l’utilisation du WCS 1,0. Cela ne signifie pas que les fonctions WCS ne retournent que ces codes d’erreur. Cela signifie que les codes du tableau ci-dessous sont retournés uniquement par les fonctions WCS. Ils peuvent également retourner d’autres codes d’erreur Win32 documentés ailleurs dans l’API Win32 du kit de développement logiciel (SDK) de plateforme.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>erreur lors de \_ la suppression \_ ICM \_ XFORM
</dt> <dd>

La transformation de couleur spécifiée n’a pas pu être supprimée.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>\_balise d’erreur dupliquée \_
</dt> <dd>

La balise d’élément de profil de couleurs spécifiée est déjà présente dans le profil de couleurs.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>erreur \_ ICM \_ non \_ activée
</dt> <dd>

La gestion des couleurs des images n’est pas activée actuellement.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERREUR \_ CMM non valide \_
</dt> <dd>

Le nom de fichier spécifié ne fait pas référence à un module de gestion de couleurs valide.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERREUR \_ COLORSPACE non valide \_
</dt> <dd>

L’espace de couleurs spécifié n’est pas valide.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERREUR \_ de \_ Profil non valide
</dt> <dd>

Le nom de fichier spécifié ne fait pas référence à un profil de couleurs valide.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERREUR \_ de \_ transformation non valide 
</dt> <dd>

La transformation de couleur qui a été spécifiée n’est pas une transformation de couleur valide.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_profil \_ d’erreur non \_ associé à l' \_ \_ appareil
</dt> <dd>

Le profil de couleurs spécifié n’est associé à aucun appareil.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_profil d' \_ erreur \_ introuvable 
</dt> <dd>

Le nom de fichier du profil de couleurs spécifié est introuvable. Le nom ou le chemin d’accès du fichier est incorrect.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_balise d’erreur \_ \_ introuvable
</dt> <dd>

La balise d’élément de profil de couleur spécifiée est introuvable dans le profil de couleurs.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>\_balise d’erreur \_ \_ absente
</dt> <dd>

Une balise d’élément de profil de couleur requise pour que la fonction aboutisse n’a pas été passée à la fonction.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Constantes WCS](wcs-constants.md)
</dt> </dl>

 

 





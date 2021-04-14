---
description: L’attribut PreviewMode spécifie le mode Aperçu pour le groupe. Si la valeur est TRUE, les frames peuvent être supprimés pendant la préversion. Dans le cas contraire, aucun cadre n’est supprimé pendant la version préliminaire. La valeur par défaut est TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Attribut PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392600"
---
# <a name="previewmode-attribute"></a>Attribut PreviewMode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `previewmode` attribut spécifie le mode Aperçu pour le groupe. Si la valeur est **true**, les frames peuvent être supprimés pendant la préversion. Dans le cas contraire, aucun cadre n’est supprimé pendant la version préliminaire. La valeur par défaut est **true**.

## <a name="possible-values"></a>Valeurs possibles

Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1. Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).

## <a name="applies-to"></a>S'applique à

[**Communauté**](group-element.md)

## <a name="remarks"></a>Notes

Dans le paramètre par défaut, les images sont supprimées lors de l’aperçu des effets ou des transitions lents, afin de maintenir la vidéo synchronisée avec l’audio. La vidéo peut paraître hachée en conséquence. L’affectation de la **valeur false** à cet attribut force chaque frame à être rendu pendant la version préliminaire, ce qui peut entraîner une désynchronisation de la vidéo avec l’audio. Les frames ne sont jamais supprimés lors de l’écriture dans un fichier.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 




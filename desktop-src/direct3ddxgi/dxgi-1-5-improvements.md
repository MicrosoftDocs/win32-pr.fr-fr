---
description: Les fonctionnalités suivantes ont été ajoutées à Microsoft DirectX Graphics infrastructure (DXGI) 1,5 pour la prise en charge de la spécification et de la duplication des formats de sortie plus flexibles.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Améliorations de DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321746"
---
# <a name="dxgi-15-improvements"></a>Améliorations de DXGI 1,5

Les fonctionnalités suivantes ont été ajoutées à Microsoft DirectX Graphics infrastructure (DXGI) 1,5 pour la prise en charge de la spécification et de la duplication des formats de sortie plus flexibles.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Plage dynamique élevée et gamme de couleurs étendue

Reportez-vous à [utilisation de DirectX avec des affichages à plage dynamique élevée et couleur avancée](../direct3darticles/high-dynamic-range.md).

## <a name="variable-refresh-rate-displays"></a>Affichage du taux d’actualisation des variables

Reportez-vous à [taux d’actualisation des variables affiche](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplication de la sortie

Une seule interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), avec une seule méthode, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), a été ajoutée à DXGI 1,5 pour fournir une version plus flexible et plus performante de la méthode [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) d’origine. **DuplicateOutput1** permet de spécifier une liste de formats pris en charge pour les surfaces plein écran qui peuvent être retournées par l’objet [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) et permet la capture de contenu HDR et WCG.

## <a name="offering-and-reclaiming-resources"></a>Offre et récupération des ressources

Les méthodes mises à jour [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) et [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) ont été ajoutées à une nouvelle interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), pour permettre la libération de la mémoire en plus de l’abandon des ressources. Si vous optez pour la nouvelle option d' [**\_ indicateur de ressource dxgi proposer la \_ \_ \_ \_ dévalidation**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) , les nouveaux résultats de la récupération doivent être correctement gérés.

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)

---
description: Gestionnaire de port vidéo
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Gestionnaire de port vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4f030e6be9035432207dc608a775a0e1d30b09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239021"
---
# <a name="video-port-manager"></a>Gestionnaire de port vidéo

Le filtre VPM (Video Port Manager Filter) permet au filtre de mélangeur vidéo 7 (VMR-7) de fonctionner avec les périphériques de capture vidéo ou les décodeurs matériels qui utilisent un port vidéo. Un port vidéo est une connexion matérielle directe à la puce graphique. Il permet de transférer la vidéo directement vers la puce graphique sans passer par le bus système.

> [!Note]  
> Le gestionnaire de port vidéo n’est pas compatible avec VMR-9, car VMR-9 ne prend pas en charge les ports vidéo.

 



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ VPVIDEO ou MEDIASUBTYPE \_ VPVBI, format \_ aucun                                                                                                                                         |
| Interfaces pin d’entrée                     | [**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Types de média de broche de sortie                   | \_Vidéo MediaType, format \_ VideoInfo2                                                                                                                                                                                 |
| Interfaces de broche de sortie                    | [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| CLSID du filtre                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [Mérite](merit.md)                       | MÉRITE \_ normal                                                                                                                                                                                                        |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Remarques

le gestionnaire de port vidéo combine la fonctionnalité de port vidéo de la [superposition Mixer le filtre](overlay-mixer-filter.md) et les fonctionnalités de l' [allocateur de Surface VBI](vbi-surface-allocator.md). Le VPM alloue des ports vidéo et des surfaces, et synchronise la capture de données à partir du port vidéo. Il autorise la capture basée sur le port vidéo qui est indépendante du rendu. Si l’aperçu est souhaité, VPM coordonne avec VMR-7 pour afficher les données de port vidéo capturées. Lorsqu’un port vidéo est présent sur le système, le filtre de capture requiert des mémoires tampons supplémentaires pour extraire les données VBI du flux vidéo. Ces mémoires tampons sont fournies par VPM. Une fois que le filtre de capture a extrait les données VBI, il les remet sur un code confidentiel distinct aux filtres tels que le décodeur CC. L’illustration suivante montre le VPM et ses connexions dans un graphique de filtre.

![segment de graphique de filtre du gestionnaire de port vidéo](images/vpm.png)

le générateur de Graph DVD ajoute automatiquement le VPM au graphique de filtre lorsqu’un port vidéo est détecté sur le système. Une fois ajouté au graphique, VPM utilise un objet DirectDraw fourni par le convertisseur de mixage vidéo pour allouer deux ou trois surfaces. Ces surfaces reçoivent les images numérisées du filtre de capture en amont. En réponse aux notifications d’événements en mode utilisateur envoyées lorsque des données sont présentes dans la surface, VPM effectue un blit automatique sur une surface hors écran fournie par VMR.

le fait que le VPM utilise plusieurs surfaces pour ses mémoires tampons d’entrée signifie qu’il nécessite plus de VRAM que l’implémentation précédente du port vidéo DirectShow. Le blit supplémentaire du VPM au VMR-7 nécessite une bande passante de mémoire vidéo supplémentaire. Et étant donné que le basculement automatique du matériel n’est plus utilisé, il existe un potentiel théorique pour les images supprimées, mais la preuve empirique suggère que cela ne se produit pas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[**Interface IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 




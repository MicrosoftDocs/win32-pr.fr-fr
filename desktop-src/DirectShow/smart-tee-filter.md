---
description: Filtre tee intelligent
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtre tee intelligent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007461"
---
# <a name="smart-tee-filter"></a>Filtre tee intelligent

Le filtre tee intelligent est utilisé dans les graphiques de capture vidéo pour fractionner le flux vidéo en un flux d’aperçu et un flux de capture. Cette opération est effectuée sans copie de données supplémentaire. Les broches de sortie prennent en charge tous les types de supports pris en charge sur la connexion en aval.

Le filtre des tees intelligents est utile lorsqu’un filtre de capture vidéo ne fournit pas de codes confidentiels distincts pour la capture et l’aperçu. Le filtre tee intelligent ne fournit des données en préversion que si cela n’a pas d’impact sur les performances de capture. Elle supprime également les horodatages du flux d’aperçu. Le générateur de graphiques de capture insère automatiquement le filtre tee intelligent si nécessaire. Pour plus d’informations, consultez combinaison de la [capture vidéo et de l’aperçu](combining-video-capture-and-preview.md).

L’illustration suivante montre un graphique de capture classique qui utilise le filtre tee intelligent.

![utilisation du filtre tee Smart](images/smarttee.png)



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Types de média de broche d’entrée                    | \_Vidéo MediaType, MEDIASUBTYPE \_ null                                                                           |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Types de média de broche de sortie                   | \_Vidéo MediaType, MEDIASUBTYPE \_ null                                                                           |
| Interfaces de broche de sortie                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | CLSID \_ SmartTee                                                                                                |
| CLSID de page de propriétés                      | Aucune page de propriétés.                                                                                              |
| Exécutable                               | qcap.dll                                                                                                       |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                            |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Notes

Le code PIN de capture est la broche de sortie 0 et le code PIN de sortie est la broche 1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




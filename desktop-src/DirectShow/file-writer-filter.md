---
description: Filtre du writer de fichier
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtre du writer de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224425"
---
# <a name="file-writer-filter"></a>Filtre du writer de fichier

Le filtre du writer de fichier peut être utilisé pour écrire des fichiers sur le disque, quel que soit le format. Le filtre écrit simplement sur le disque quelle que soit sa broche d’entrée, il doit donc être connecté en amont à un multiplexeur capable de mettre en forme le fichier correctement. Vous pouvez créer un nouveau fichier de sortie avec le writer de fichier ou spécifier un fichier existant ; Si le fichier existe déjà, il sera entièrement remplacé par les nouvelles données.

Le filtre du writer de fichier utilise les horodatages du flux d’entrée comme décalages de fichiers et fournit un accès aléatoire au fichier. Il prend en charge **IStream** pour autoriser la lecture et l’écriture de l’en-tête de fichier une fois que le graphique est arrêté. Pour améliorer les performances, il prend également en charge les écritures avec chevauchement non mises en mémoire tampon et gère la négociation de mémoire tampon correspondante.

> [!Note]  
> Pour écrire des fichiers ASF, utilisez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) .

 



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream** |
| Types de média de broche d’entrée                    | \_Flux de MediaType, MEDIASUBTYPE \_ null                                                                                                                                                              |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Types de média de broche de sortie                   | Non applicable                                                                                                                                                                                     |
| Interfaces de broche de sortie                    | Non applicable                                                                                                                                                                                     |
| CLSID du filtre                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                                                                   |
| Exécutable                               | qcap.dll                                                                                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ n' \_ \_ utilise pas                                                                                                                                                                                |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 




---
description: Le filtre de convertisseur MIDI effectue le rendu des données MIDI à partir du filtre de l’analyseur MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: filtre de convertisseur MIDI (Windows. devices. midi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 3727fb322e03338723eb3c9da1ac86d4e6a7145424cb04b0c050b67f83aa141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791449"
---
# <a name="midi-renderer-filter"></a>Filtre de convertisseur MIDI

Le filtre de convertisseur MIDI effectue le rendu des données MIDI à partir du filtre de l' [analyseur midi](midi-parser-filter.md) .



| Étiquette | Valeur |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Types de média de broche d’entrée                    | \_Midi MediaType, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                                                                                                                  |
| Interfaces pin d’entrée                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Types de média de broche de sortie                   | Non applicable                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de broche de sortie                    | Non applicable                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID du filtre                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                                                                                                                                                                                                                                                                                                     |
| Exécutable                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Mérite](merit.md)                       | MÉRITE \_ préféré                                                                                                                                                                                                                                                                                                                                                                     |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ MidiRendererCategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Remarques

Le GUID du type de format est **null**, mais le bloc de format contient la structure suivante :


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Le membre **dwDivision** spécifie la Division de temps du fichier. La Division de l’heure est donnée dans l’en-tête de n’importe quel fichier MIDI standard (SMF) dans le `MThd` bloc. Le convertisseur MIDI définit cette propriété sur le flux de données MIDI en appelant la fonction **midiStreamProperty** .

Les exemples du filtre de l’analyseur MIDI contiennent une seconde de données MIDI. Le convertisseur MIDI utilise la fonction **midiStreamOut** pour effectuer le rendu des données MIDI. Chaque échantillon est un point de synchronisation : le début de la mémoire tampon contient toutes les commandes nécessaires pour définir l’état correct pour le rendu de cette mémoire tampon.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Windows. devices. midi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 





---
description: Le filtre de convertisseur MIDI effectue le rendu des données MIDI à partir du filtre de l’analyseur MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: Filtre de convertisseur MIDI (Windows. Devices. midi. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529964"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="f779d-103">Filtre de convertisseur MIDI</span><span class="sxs-lookup"><span data-stu-id="f779d-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="f779d-104">Le filtre de convertisseur MIDI effectue le rendu des données MIDI à partir du filtre de l' [analyseur midi](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f779d-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f779d-105">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f779d-105">Filter Interfaces</span></span>                        | <span data-ttu-id="f779d-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="f779d-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="f779d-107">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f779d-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="f779d-108">\_Midi MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="f779d-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f779d-109">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f779d-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f779d-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f779d-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f779d-111">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f779d-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="f779d-112">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f779d-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f779d-113">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f779d-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f779d-114">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f779d-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f779d-115">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f779d-115">Filter CLSID</span></span>                             | <span data-ttu-id="f779d-116">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="f779d-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f779d-117">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f779d-117">Property Page CLSID</span></span>                      | <span data-ttu-id="f779d-118">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f779d-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f779d-119">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f779d-119">Executable</span></span>                               | <span data-ttu-id="f779d-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f779d-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f779d-121">Mérite</span><span class="sxs-lookup"><span data-stu-id="f779d-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="f779d-122">MÉRITE \_ préféré</span><span class="sxs-lookup"><span data-stu-id="f779d-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f779d-123">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="f779d-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f779d-124">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="f779d-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f779d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f779d-125">Remarks</span></span>

<span data-ttu-id="f779d-126">Le GUID du type de format est **null**, mais le bloc de format contient la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="f779d-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="f779d-127">Le membre **dwDivision** spécifie la Division de temps du fichier.</span><span class="sxs-lookup"><span data-stu-id="f779d-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="f779d-128">La Division de l’heure est donnée dans l’en-tête de n’importe quel fichier MIDI standard (SMF) dans le `MThd` bloc.</span><span class="sxs-lookup"><span data-stu-id="f779d-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="f779d-129">Le convertisseur MIDI définit cette propriété sur le flux de données MIDI en appelant la fonction **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="f779d-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="f779d-130">Les exemples du filtre de l’analyseur MIDI contiennent une seconde de données MIDI.</span><span class="sxs-lookup"><span data-stu-id="f779d-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="f779d-131">Le convertisseur MIDI utilise la fonction **midiStreamOut** pour effectuer le rendu des données MIDI.</span><span class="sxs-lookup"><span data-stu-id="f779d-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="f779d-132">Chaque échantillon est un point de synchronisation : le début de la mémoire tampon contient toutes les commandes nécessaires pour définir l’état correct pour le rendu de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f779d-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f779d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f779d-133">Requirements</span></span>



| <span data-ttu-id="f779d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f779d-134">Requirement</span></span> | <span data-ttu-id="f779d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="f779d-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f779d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f779d-136">Header</span></span><br/> | <dl> <span data-ttu-id="f779d-137"><dt>Windows. Devices. midi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f779d-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f779d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f779d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f779d-139">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f779d-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 





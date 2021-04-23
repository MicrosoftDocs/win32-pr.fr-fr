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
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909407"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="ebadd-103">Filtre de convertisseur MIDI</span><span class="sxs-lookup"><span data-stu-id="ebadd-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="ebadd-104">Le filtre de convertisseur MIDI effectue le rendu des données MIDI à partir du filtre de l' [analyseur midi](midi-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ebadd-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="ebadd-105">Étiquette</span><span class="sxs-lookup"><span data-stu-id="ebadd-105">Label</span></span> | <span data-ttu-id="ebadd-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebadd-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebadd-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="ebadd-107">Filter Interfaces</span></span>                        | <span data-ttu-id="ebadd-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="ebadd-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="ebadd-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="ebadd-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="ebadd-110">\_Midi MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="ebadd-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ebadd-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="ebadd-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ebadd-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ebadd-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ebadd-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ebadd-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="ebadd-114">Non applicable</span><span class="sxs-lookup"><span data-stu-id="ebadd-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ebadd-115">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ebadd-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ebadd-116">Non applicable</span><span class="sxs-lookup"><span data-stu-id="ebadd-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ebadd-117">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="ebadd-117">Filter CLSID</span></span>                             | <span data-ttu-id="ebadd-118">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="ebadd-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ebadd-119">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ebadd-119">Property Page CLSID</span></span>                      | <span data-ttu-id="ebadd-120">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ebadd-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ebadd-121">Exécutable</span><span class="sxs-lookup"><span data-stu-id="ebadd-121">Executable</span></span>                               | <span data-ttu-id="ebadd-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="ebadd-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ebadd-123">Mérite</span><span class="sxs-lookup"><span data-stu-id="ebadd-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="ebadd-124">MÉRITE \_ préféré</span><span class="sxs-lookup"><span data-stu-id="ebadd-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ebadd-125">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="ebadd-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ebadd-126">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="ebadd-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="ebadd-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebadd-127">Remarks</span></span>

<span data-ttu-id="ebadd-128">Le GUID du type de format est **null**, mais le bloc de format contient la structure suivante :</span><span class="sxs-lookup"><span data-stu-id="ebadd-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="ebadd-129">Le membre **dwDivision** spécifie la Division de temps du fichier.</span><span class="sxs-lookup"><span data-stu-id="ebadd-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="ebadd-130">La Division de l’heure est donnée dans l’en-tête de n’importe quel fichier MIDI standard (SMF) dans le `MThd` bloc.</span><span class="sxs-lookup"><span data-stu-id="ebadd-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="ebadd-131">Le convertisseur MIDI définit cette propriété sur le flux de données MIDI en appelant la fonction **midiStreamProperty** .</span><span class="sxs-lookup"><span data-stu-id="ebadd-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="ebadd-132">Les exemples du filtre de l’analyseur MIDI contiennent une seconde de données MIDI.</span><span class="sxs-lookup"><span data-stu-id="ebadd-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="ebadd-133">Le convertisseur MIDI utilise la fonction **midiStreamOut** pour effectuer le rendu des données MIDI.</span><span class="sxs-lookup"><span data-stu-id="ebadd-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="ebadd-134">Chaque échantillon est un point de synchronisation : le début de la mémoire tampon contient toutes les commandes nécessaires pour définir l’état correct pour le rendu de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ebadd-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebadd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebadd-135">Requirements</span></span>



| <span data-ttu-id="ebadd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebadd-136">Requirement</span></span> | <span data-ttu-id="ebadd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebadd-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebadd-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebadd-138">Header</span></span><br/> | <dl> <span data-ttu-id="ebadd-139"><dt>Windows. Devices. midi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebadd-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebadd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebadd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebadd-141">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="ebadd-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 





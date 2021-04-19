---
title: Types de données d’entrée MIDI
description: Types de données d’entrée MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Interface MIDI (Musical Instrument Digital Interface), types de données d’entrée
- MIDI (Musical Instrument Digital Interface), types de données d’entrée
- enregistrement d’un fichier audio MIDI, types de données d’entrée
- Types de données d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510064"
---
# <a name="midi-input-data-types"></a><span data-ttu-id="502ff-107">Types de données d’entrée MIDI</span><span class="sxs-lookup"><span data-stu-id="502ff-107">MIDI Input Data Types</span></span>

<span data-ttu-id="502ff-108">Windows définit les types de données suivants pour les fonctions d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="502ff-108">Windows defines the following data types for the MIDI input functions.</span></span>



| <span data-ttu-id="502ff-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="502ff-109">Value</span></span>                            | <span data-ttu-id="502ff-110">Signification</span><span class="sxs-lookup"><span data-stu-id="502ff-110">Meaning</span></span>                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="502ff-111">**HMIDIIN**</span><span class="sxs-lookup"><span data-stu-id="502ff-111">**HMIDIIN**</span></span>                      | <span data-ttu-id="502ff-112">Handle d’un appareil d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="502ff-112">Handle of a MIDI input device.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="502ff-113">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="502ff-113">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | <span data-ttu-id="502ff-114">En-tête pour une mémoire tampon de flux ou un bloc de données système-exclusives MIDI.</span><span class="sxs-lookup"><span data-stu-id="502ff-114">Header for a stream buffer or a block of MIDI system-exclusive data.</span></span> <span data-ttu-id="502ff-115">Pour les applications d’entrée, cette structure enregistre uniquement les données système exclusives (la diffusion en continu n’est pas prise en charge pour l’entrée MIDI).</span><span class="sxs-lookup"><span data-stu-id="502ff-115">For input applications, this structure records only system-exclusive data (streaming is not supported for MIDI input).</span></span> |
| [<span data-ttu-id="502ff-116">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="502ff-116">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | <span data-ttu-id="502ff-117">Structure utilisée pour se renseigner sur les fonctionnalités d’un appareil d’entrée MIDI.</span><span class="sxs-lookup"><span data-stu-id="502ff-117">Structure used to inquire about the capabilities of a MIDI input device.</span></span>                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="502ff-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="502ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="502ff-119">Enregistrement d’un fichier audio MIDI</span><span class="sxs-lookup"><span data-stu-id="502ff-119">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 
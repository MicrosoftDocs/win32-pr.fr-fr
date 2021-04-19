---
title: Gestion des erreurs avec les fonctions MIDI
description: Gestion des erreurs avec les fonctions MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- MIDI (Musical Instrument Digital Interface), Erreurs
- MIDI (Musical Instrument Digital Interface), Erreurs
- Services MIDI, Erreurs
- Erreurs MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510471"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="501fa-107">Gestion des erreurs avec les fonctions MIDI</span><span class="sxs-lookup"><span data-stu-id="501fa-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="501fa-108">Les fonctions audio MIDI retournent un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="501fa-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="501fa-109">Pour les erreurs associées à MIDI, les fonctions [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) et [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) récupèrent les descriptions textuelles des codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="501fa-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="501fa-110">L’application doit toujours examiner la valeur d’erreur elle-même pour déterminer comment procéder, mais elle peut utiliser les descriptions d’erreur dans les boîtes de dialogue pour informer les utilisateurs des conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="501fa-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="501fa-111">Les seules fonctions MIDI qui ne retournent pas de codes d’erreur sont les fonctions [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) et [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="501fa-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="501fa-112">Ces fonctions retournent une valeur de zéro si aucun appareil n’est présent dans un système ou si des erreurs sont rencontrées par la fonction.</span><span class="sxs-lookup"><span data-stu-id="501fa-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="501fa-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="501fa-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="501fa-114">Services MIDI</span><span class="sxs-lookup"><span data-stu-id="501fa-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 
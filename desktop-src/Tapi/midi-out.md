---
description: La classe de périphérique MIDI/Out est composée de séquenceurs MIDI utilisés pour la sortie. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201207"
---
# <a name="midiout"></a><span data-ttu-id="2892c-104">midi/out</span><span class="sxs-lookup"><span data-stu-id="2892c-104">midi/out</span></span>

<span data-ttu-id="2892c-105">La classe de périphérique MIDI/Out est composée de séquenceurs MIDI utilisés pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="2892c-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="2892c-106">Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="2892c-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="2892c-107">Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="2892c-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="2892c-108">Le membre **DeviceID** est l’identificateur d’un appareil midi fermé.</span><span class="sxs-lookup"><span data-stu-id="2892c-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="2892c-109">Vous utilisez cet identificateur dans un appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) pour ouvrir l’appareil pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="2892c-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="2892c-110">Vous pouvez utiliser le handle d’appareil résultant pour lire les données MIDI sur la ligne ou l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="2892c-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="2892c-111">Pour plus d’informations sur les fonctions MIDI, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2892c-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 

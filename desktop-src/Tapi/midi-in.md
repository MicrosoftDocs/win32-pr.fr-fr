---
description: La classe d’appareils midi/in est constituée de séquences MIDI utilisées pour l’entrée. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749540"
---
# <a name="midiin"></a><span data-ttu-id="ca01f-104">midi/in</span><span class="sxs-lookup"><span data-stu-id="ca01f-104">midi/in</span></span>

<span data-ttu-id="ca01f-105">La classe d’appareils midi/in est constituée de séquences MIDI utilisées pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="ca01f-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="ca01f-106">Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ca01f-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="ca01f-107">Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="ca01f-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="ca01f-108">Le membre **DeviceID** est l’identificateur d’un appareil midi fermé.</span><span class="sxs-lookup"><span data-stu-id="ca01f-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="ca01f-109">Vous utilisez cet identificateur dans un appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) pour ouvrir l’appareil pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="ca01f-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="ca01f-110">Vous pouvez utiliser le handle d’appareil résultant pour enregistrer les données MIDI à partir de la ligne ou du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="ca01f-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="ca01f-111">Pour plus d’informations sur les fonctions MIDI, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ca01f-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 

---
description: La classe de périphérique Wave/out est constituée de périphériques audio pour une sortie audio Wave de bas niveau.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869186"
---
# <a name="waveout"></a><span data-ttu-id="bf659-103">Wave/sortie</span><span class="sxs-lookup"><span data-stu-id="bf659-103">wave/out</span></span>

<span data-ttu-id="bf659-104">La classe de périphérique Wave/out est constituée de périphériques audio pour une sortie audio Wave de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="bf659-104">The wave/out device class consists of audio devices for low-level wave audio output.</span></span> <span data-ttu-id="bf659-105">Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="bf659-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="bf659-106">Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="bf659-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="bf659-107">Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="bf659-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="bf659-108">Le membre **DeviceID** est l’identificateur d’un périphérique audio fermé.</span><span class="sxs-lookup"><span data-stu-id="bf659-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="bf659-109">Vous utilisez cet identificateur dans un appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir l’appareil pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="bf659-109">You use this identifier in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="bf659-110">Vous pouvez utiliser le handle d’appareil obtenu pour lire les données audio numérisées sur la ligne ou le périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="bf659-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="bf659-111">Bien qu’une classe d’appareil « Wave » existe également pour les périphériques audio Wave de bas niveau, vous devez toujours utiliser la classe de périphérique Wave/sortie pour une sortie d’onde de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="bf659-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/out device class for low-level wave output.</span></span>

<span data-ttu-id="bf659-112">Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 

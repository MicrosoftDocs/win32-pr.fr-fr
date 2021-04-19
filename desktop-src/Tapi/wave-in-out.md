---
description: La classe d’appareils Wave/entrée/sortie se compose de périphériques audio duplex intégral.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/entrée/sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541840"
---
# <a name="waveinout"></a><span data-ttu-id="a022f-103">Wave/entrée/sortie</span><span class="sxs-lookup"><span data-stu-id="a022f-103">wave/in/out</span></span>

<span data-ttu-id="a022f-104">La classe d’appareils Wave/entrée/sortie se compose de périphériques audio duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="a022f-104">The wave/in/out device class consists of full duplex audio devices.</span></span> <span data-ttu-id="a022f-105">Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="a022f-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="a022f-106">Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="a022f-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="a022f-107">Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant deux membres supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="a022f-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending two additional members:</span></span>

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

<span data-ttu-id="a022f-108">Les membres **DeviceInId** et **DeviceOutId** sont des identificateurs d’un périphérique audio fermé.</span><span class="sxs-lookup"><span data-stu-id="a022f-108">The **DeviceInId** and **DeviceOutId** members are identifiers of a closed audio device.</span></span> <span data-ttu-id="a022f-109">Vous utilisez ces identificateurs dans un appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir l’appareil pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="a022f-109">You use these identifiers in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="a022f-110">Vous pouvez utiliser le handle d’appareil obtenu pour lire les données audio numérisées sur la ligne ou le périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="a022f-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="a022f-111">Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a022f-111">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 

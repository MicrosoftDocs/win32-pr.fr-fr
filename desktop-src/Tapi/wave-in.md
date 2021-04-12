---
description: La classe d’appareils Wave/in est constituée de périphériques audio pour une entrée audio Wave de bas niveau.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209998"
---
# <a name="wavein"></a><span data-ttu-id="81315-103">Wave/entrée</span><span class="sxs-lookup"><span data-stu-id="81315-103">wave/in</span></span>

<span data-ttu-id="81315-104">La classe d’appareils Wave/in est constituée de périphériques audio pour une entrée audio Wave de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="81315-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="81315-105">Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="81315-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="81315-106">Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="81315-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="81315-107">Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="81315-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="81315-108">Le membre **DeviceID** est l’identificateur d’un périphérique audio fermé.</span><span class="sxs-lookup"><span data-stu-id="81315-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="81315-109">Vous utilisez cet identificateur dans un appel à la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) pour ouvrir l’appareil pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="81315-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="81315-110">Vous pouvez utiliser le handle de périphérique résultant pour enregistrer des données audio numérisées à partir de la ligne ou du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="81315-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="81315-111">Bien qu’une classe d’appareil « Wave » existe également pour les périphériques audio Wave de bas niveau, vous devez toujours utiliser la classe de périphérique Wave/in pour une entrée Wave de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="81315-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="81315-112">Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="81315-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 

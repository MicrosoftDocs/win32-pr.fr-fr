---
description: La classe d’appareil TAPI/terminal se compose des appareils téléphoniques associés à chaque terminal sur une ligne ou le terminal sur chaque ligne associée à un appareil téléphonique. Vous accédez à ces appareils à l’aide des fonctions de périphérique de ligne TAPI ou de téléphone.
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: TAPI/terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534644"
---
# <a name="tapiterminal"></a><span data-ttu-id="71e6c-104">TAPI/terminal</span><span class="sxs-lookup"><span data-stu-id="71e6c-104">tapi/terminal</span></span>

<span data-ttu-id="71e6c-105">La classe d’appareil TAPI/terminal se compose des appareils téléphoniques associés à chaque terminal sur une ligne ou le terminal sur chaque ligne associée à un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="71e6c-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="71e6c-106">Vous accédez à ces appareils à l’aide des fonctions de périphérique de [ligne](line-device-functions.md) TAPI ou de [téléphone](phone-device-functions.md).</span><span class="sxs-lookup"><span data-stu-id="71e6c-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="71e6c-107">La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="71e6c-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="71e6c-108">Le membre **adwDeviceId** est un tableau d’identificateurs de périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="71e6c-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="71e6c-109">Il existe un élément de tableau pour chaque terminal spécifié par le membre **dwNumTerminals** dans la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="71e6c-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="71e6c-110">Chaque élément spécifie l’identificateur de l’appareil téléphonique associé au terminal correspondant sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="71e6c-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="71e6c-111">Si aucun appareil téléphonique n’est associé à un terminal, l’élément est défini sur-1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="71e6c-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="71e6c-112">La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="71e6c-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="71e6c-113">Le membre **adwTerminalID** est un tableau d’identificateurs de terminal.</span><span class="sxs-lookup"><span data-stu-id="71e6c-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="71e6c-114">Il y a un élément de tableau pour chaque identificateur de périphérique de ligne spécifié par la fonction [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .</span><span class="sxs-lookup"><span data-stu-id="71e6c-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="71e6c-115">Chaque élément de tableau contient l’identificateur de terminal associé à l’appareil téléphonique pour l’appareil de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="71e6c-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="71e6c-116">S’il n’y a pas d’appareil téléphonique, l’élément est défini sur-1 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="71e6c-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="71e6c-117">La valeur de la plage des identificateurs de terminal est comprise entre zéro et un nombre inférieur au nombre spécifié par le membre **dwNumTerminals** dans la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="71e6c-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 




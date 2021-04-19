---
description: La classe d’appareil TAPI/Line se compose de tous les appareils en ligne. Vous accédez à ces appareils à l’aide des fonctions de ligne TAPI.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530679"
---
# <a name="tapiline"></a><span data-ttu-id="76d79-104">TAPI/ligne</span><span class="sxs-lookup"><span data-stu-id="76d79-104">tapi/line</span></span>

<span data-ttu-id="76d79-105">La classe d’appareil TAPI/Line se compose de tous les appareils en ligne.</span><span class="sxs-lookup"><span data-stu-id="76d79-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="76d79-106">Vous accédez à ces appareils à l’aide des fonctions de ligne TAPI.</span><span class="sxs-lookup"><span data-stu-id="76d79-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="76d79-107">La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="76d79-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="76d79-108">Le membre **dwDeviceId** est l’identificateur de l’appareil de ligne associé au handle de ligne donné par [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span><span class="sxs-lookup"><span data-stu-id="76d79-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="76d79-109">La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit également une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant **dwStringFormat** sur STRINGFORMAT \_ Binary et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="76d79-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="76d79-110">Le membre **adwDeviceIds** est un tableau contenant les identificateurs de périphérique de tous les périphériques de ligne associés à l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="76d79-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="76d79-111">S’il n’y a pas d’appareils de ligne associés, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) retourne la \_ valeur INVALDEVICECLASS PHONEERR.</span><span class="sxs-lookup"><span data-stu-id="76d79-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 




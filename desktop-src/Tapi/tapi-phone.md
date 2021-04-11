---
description: La classe de l’appareil TAPI/Phone est composée de tous les appareils téléphoniques. Vous accédez à ces appareils à l’aide des fonctions de téléphone TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952478"
---
# <a name="tapiphone"></a><span data-ttu-id="ab4a9-104">TAPI/téléphone</span><span class="sxs-lookup"><span data-stu-id="ab4a9-104">tapi/phone</span></span>

<span data-ttu-id="ab4a9-105">La classe de l’appareil TAPI/Phone est composée de tous les appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="ab4a9-106">Vous accédez à ces appareils à l’aide des fonctions de téléphone TAPI.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="ab4a9-107">La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="ab4a9-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="ab4a9-108">Le membre **dwDeviceId** est l’identificateur de l’appareil téléphonique associé au descripteur téléphonique donné par [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span><span class="sxs-lookup"><span data-stu-id="ab4a9-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="ab4a9-109">La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit également une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant **dwStringFormat** sur STRINGFORMAT \_ Binary et en ajoutant ce membre supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="ab4a9-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="ab4a9-110">Le membre **adwDeviceIds** est un tableau contenant les identificateurs de périphérique de tous les appareils téléphoniques associés à l’appareil de ligne donné.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="ab4a9-111">Si aucun appareil téléphonique n’est associé, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) retourne la \_ valeur INVALDEVICECLASS LINEERR.</span><span class="sxs-lookup"><span data-stu-id="ab4a9-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 




---
description: La classe de l’appareil TAPI/Phone est composée de tous les appareils téléphoniques. Vous accédez à ces appareils à l’aide des fonctions de téléphone TAPI.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b3238fb2e83d4f6e5e565f40b3ab3b124236ae2c89f879cb284d4a5997f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002717"
---
# <a name="tapiphone"></a>TAPI/téléphone

La classe de l’appareil TAPI/Phone est composée de tous les appareils téléphoniques. Vous accédez à ces appareils à l’aide des fonctions de téléphone TAPI.

La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

Le membre **dwDeviceId** est l’identificateur de l’appareil téléphonique associé au descripteur téléphonique donné par [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).

La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit également une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant **dwStringFormat** sur STRINGFORMAT \_ Binary et en ajoutant ce membre supplémentaire :

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

Le membre **adwDeviceIds** est un tableau contenant les identificateurs de périphérique de tous les appareils téléphoniques associés à l’appareil de ligne donné. Si aucun appareil téléphonique n’est associé, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) retourne la \_ valeur INVALDEVICECLASS LINEERR.

 

 




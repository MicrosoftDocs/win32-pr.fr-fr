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
# <a name="tapiline"></a>TAPI/ligne

La classe d’appareil TAPI/Line se compose de tous les appareils en ligne. Vous accédez à ces appareils à l’aide des fonctions de ligne TAPI.

La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire.

``` syntax
DWORD dwDeviceI;  // line device identifier
```

Le membre **dwDeviceId** est l’identificateur de l’appareil de ligne associé au handle de ligne donné par [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).

La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit également une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant **dwStringFormat** sur STRINGFORMAT \_ Binary et en ajoutant ce membre supplémentaire :

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

Le membre **adwDeviceIds** est un tableau contenant les identificateurs de périphérique de tous les périphériques de ligne associés à l’appareil téléphonique. S’il n’y a pas d’appareils de ligne associés, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) retourne la \_ valeur INVALDEVICECLASS PHONEERR.

 

 




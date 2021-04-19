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
# <a name="tapiterminal"></a>TAPI/terminal

La classe d’appareil TAPI/terminal se compose des appareils téléphoniques associés à chaque terminal sur une ligne ou le terminal sur chaque ligne associée à un appareil téléphonique. Vous accédez à ces appareils à l’aide des fonctions de périphérique de [ligne](line-device-functions.md) TAPI ou de [téléphone](phone-device-functions.md).

La fonction [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

Le membre **adwDeviceId** est un tableau d’identificateurs de périphérique téléphonique. Il existe un élément de tableau pour chaque terminal spécifié par le membre **dwNumTerminals** dans la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne donné. Chaque élément spécifie l’identificateur de l’appareil téléphonique associé au terminal correspondant sur la ligne. Si aucun appareil téléphonique n’est associé à un terminal, l’élément est défini sur-1 (0xFFFFFFFF).

La fonction [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplit une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **DWSTRINGFORMAT** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

Le membre **adwTerminalID** est un tableau d’identificateurs de terminal. Il y a un élément de tableau pour chaque identificateur de périphérique de ligne spécifié par la fonction [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) . Chaque élément de tableau contient l’identificateur de terminal associé à l’appareil téléphonique pour l’appareil de ligne donné. S’il n’y a pas d’appareil téléphonique, l’élément est défini sur-1 (0xFFFFFFFF). La valeur de la plage des identificateurs de terminal est comprise entre zéro et un nombre inférieur au nombre spécifié par le membre **dwNumTerminals** dans la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .

 

 




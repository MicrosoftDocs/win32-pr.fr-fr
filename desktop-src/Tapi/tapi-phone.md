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

 

 




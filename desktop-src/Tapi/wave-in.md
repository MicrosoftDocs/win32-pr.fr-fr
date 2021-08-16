---
description: La classe d’appareils Wave/in est constituée de périphériques audio pour une entrée audio Wave de bas niveau.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: Wave/entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24cc80d41f402abf1886e063563f272abf7992768dd62f03e64b327a7e199360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002527"
---
# <a name="wavein"></a>Wave/entrée

La classe d’appareils Wave/in est constituée de périphériques audio pour une entrée audio Wave de bas niveau. Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme. Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Le membre **DeviceID** est l’identificateur d’un périphérique audio fermé. Vous utilisez cet identificateur dans un appel à la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) pour ouvrir l’appareil pour l’entrée. Vous pouvez utiliser le handle de périphérique résultant pour enregistrer des données audio numérisées à partir de la ligne ou du périphérique téléphonique.

Bien qu’une classe d’appareil « Wave » existe également pour les périphériques audio Wave de bas niveau, vous devez toujours utiliser la classe de périphérique Wave/in pour une entrée Wave de bas niveau.

Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).

 

 

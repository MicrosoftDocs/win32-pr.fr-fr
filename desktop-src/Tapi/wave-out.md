---
description: La classe de périphérique Wave/out est constituée de périphériques audio pour une sortie audio Wave de bas niveau.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: Wave/sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3e8a82b8345e8f50e1ad18f527c82f4ece241e03c0ea7cd083dd2d2ae79282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760174"
---
# <a name="waveout"></a>Wave/sortie

La classe de périphérique Wave/out est constituée de périphériques audio pour une sortie audio Wave de bas niveau. Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme. Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD DeviceId;  // identifier of audio device
```

Le membre **DeviceID** est l’identificateur d’un périphérique audio fermé. Vous utilisez cet identificateur dans un appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir l’appareil pour la sortie. Vous pouvez utiliser le handle d’appareil obtenu pour lire les données audio numérisées sur la ligne ou le périphérique téléphonique.

Bien qu’une classe d’appareil « Wave » existe également pour les périphériques audio Wave de bas niveau, vous devez toujours utiliser la classe de périphérique Wave/sortie pour une sortie d’onde de bas niveau.

Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).

 

 

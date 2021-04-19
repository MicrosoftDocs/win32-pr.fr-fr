---
description: La classe d’appareils Wave/entrée/sortie se compose de périphériques audio duplex intégral.
ms.assetid: 1b49c9ae-da64-4415-95ce-785ffedc65bc
title: Wave/entrée/sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e814cf2e8de1c3c5700a7570d2ed2b4c428572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541840"
---
# <a name="waveinout"></a>Wave/entrée/sortie

La classe d’appareils Wave/entrée/sortie se compose de périphériques audio duplex intégral. Vous accédez à ces appareils à l’aide des fonctions Wave, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme. Les appareils de cette classe sont associés à des appareils de ligne qui prennent en charge le \_ type de média LINEMEDIAMODE AUTOMATEDVOICE, qui est spécifié dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour le périphérique de ligne.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant deux membres supplémentaires :

``` syntax
DWORD DeviceInId;  // identifier of wave in audio device
DWORD DeviceOutId;  // identifier of wave out audio device
```

Les membres **DeviceInId** et **DeviceOutId** sont des identificateurs d’un périphérique audio fermé. Vous utilisez ces identificateurs dans un appel à la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) pour ouvrir l’appareil pour la sortie. Vous pouvez utiliser le handle d’appareil obtenu pour lire les données audio numérisées sur la ligne ou le périphérique téléphonique.

Pour plus d’informations sur les fonctions Wave, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).

 

 

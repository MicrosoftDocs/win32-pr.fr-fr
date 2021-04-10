---
description: La classe de périphérique MIDI/Out est composée de séquenceurs MIDI utilisés pour la sortie. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201207"
---
# <a name="midiout"></a>midi/out

La classe de périphérique MIDI/Out est composée de séquenceurs MIDI utilisés pour la sortie. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Le membre **DeviceID** est l’identificateur d’un appareil midi fermé. Vous utilisez cet identificateur dans un appel à la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) pour ouvrir l’appareil pour la sortie. Vous pouvez utiliser le handle d’appareil résultant pour lire les données MIDI sur la ligne ou l’appareil téléphonique.

Pour plus d’informations sur les fonctions MIDI, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).

 

 

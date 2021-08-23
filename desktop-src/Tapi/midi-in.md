---
description: La classe d’appareils midi/in est constituée de séquences MIDI utilisées pour l’entrée. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659949"
---
# <a name="midiin"></a>midi/in

La classe d’appareils midi/in est constituée de séquences MIDI utilisées pour l’entrée. Vous accédez à ces appareils à l’aide des fonctions MIDI, qui sont décrites dans le kit de développement logiciel (SDK) de la plateforme.

Les fonctions [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) et [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) remplissent une structure [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , en définissant le membre **dwStringFormat** sur la \_ valeur binaire STRINGFORMAT et en ajoutant ce membre supplémentaire :

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Le membre **DeviceID** est l’identificateur d’un appareil midi fermé. Vous utilisez cet identificateur dans un appel à la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) pour ouvrir l’appareil pour l’entrée. Vous pouvez utiliser le handle d’appareil résultant pour enregistrer les données MIDI à partir de la ligne ou du périphérique téléphonique.

Pour plus d’informations sur les fonctions MIDI, consultez [**fonctions multimédias**](../multimedia/multimedia-functions.md).

 

 

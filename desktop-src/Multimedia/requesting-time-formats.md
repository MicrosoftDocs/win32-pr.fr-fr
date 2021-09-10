---
title: Demande de formats d’heure
description: Demande de formats d’heure
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (Musical Instrument Digital Interface), formats d’heure
- MIDI (Musical Instrument Digital Interface), formats d’heure
- Services MIDI, formats d’heure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364451"
---
# <a name="requesting-time-formats"></a>Demande de formats d’heure

Windows utilise la structure [**MMTIME**](/previous-versions//dd757347(v=vs.85)) pour représenter le temps dans un ou plusieurs formats différents, y compris les millisecondes, les exemples, les formats de pointeur de chanson et les pointeurs MIDI. Le membre **wType** spécifie le format d’heure.

La fonction [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) utilise la structure **MMTIME** . Avant d’appeler cette fonction, vous devez définir le membre **wType** pour indiquer le format d’heure demandé. Pour voir si le format d’heure demandé est pris en charge, vérifiez **wType** après l’appel. Si le format d’heure demandé n’est pas pris en charge, l’heure est spécifiée dans un autre format d’heure sélectionné par le pilote de périphérique et le membre **wType** est modifié pour indiquer le format d’heure sélectionné.

Pour plus d’informations sur la structure **MMTIME** , consultez [minuteries multimédias](multimedia-timers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 
---
title: Gestion des blocs de données par interrogation
description: Gestion des blocs de données par interrogation
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- sons Waveform, interrogation des blocs de données
- blocs de données audio, interrogation
- interrogation des blocs de données audio
- WAVEHDR, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c84e75eccaf34ef16ccadefb4dae42931854a0c6c4278003fb5c01b0c551f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139164"
---
# <a name="managing-data-blocks-by-polling"></a>Gestion des blocs de données par interrogation

Outre l’utilisation d’une fonction de rappel, vous pouvez interroger le membre **dwFlags** d’une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pour déterminer quand un périphérique audio est terminé avec un bloc de données. Il est parfois préférable d’interroger **dwFlags** plutôt que d’attendre qu’un autre mécanisme reçoit des messages des pilotes. Par exemple, après avoir appelé la fonction [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) pour libérer des blocs de données en attente, vous pouvez immédiatement interroger pour vous assurer que les blocs de données ont été libérés avant d’appeler [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) et de libérer de la mémoire pour le bloc de données.

Vous pouvez utiliser l' \_ indicateur WHDR Done pour tester le membre **dwFlags** . Dès que l’indicateur WHDR \_ done est défini dans le membre **dwFlags** de la structure **WAVEHDR** , le pilote est terminé avec le bloc de données.

 

 
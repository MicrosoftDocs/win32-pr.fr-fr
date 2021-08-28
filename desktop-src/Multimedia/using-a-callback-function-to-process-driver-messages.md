---
title: Utilisation d’une fonction de rappel pour traiter des messages de pilote
description: Utilisation d’une fonction de rappel pour traiter des messages de pilote
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- sons Waveform, fonctions de rappel
- blocs de données audio, fonctions de rappel
- audio Wave, traitement des messages de pilote
- blocs de données audio, traitement des messages de pilote
- traitement des messages du pilote
- waveInOpen fonction)
- waveOutOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf386c517d900fc4b0450f169060c6be6365df57ab0fcb3e6953337f4f67fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892429"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>Utilisation d’une fonction de rappel pour traiter des messages de pilote

Vous pouvez écrire votre propre fonction de rappel pour traiter les messages envoyés par le pilote de périphérique. Pour utiliser une fonction de rappel, spécifiez l’indicateur de fonction de rappel \_ dans le paramètre *fdwOpen* et l’adresse du rappel dans le paramètre *DwCallback* de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

Les messages envoyés à une fonction de rappel sont similaires aux messages envoyés à une fenêtre, sauf qu’ils ont deux paramètres **DWORD** au lieu d’un paramètre **uint** et d’un paramètre **DWORD** . Pour plus d’informations sur ces messages, consultez [playing Waveform-Audio Files](playing-waveform-audio-files.md).

Pour passer des données d’instance d’une application à une fonction de rappel, utilisez l’une des techniques suivantes :

-   Transmettez les données de l’instance à l’aide du paramètre *dwInstance* de la fonction qui ouvre le pilote de périphérique.
-   Transmettez les données d’instance à l’aide du membre **dwUser** de la structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie un bloc de données audio envoyé à un pilote de périphérique.

Si vous avez besoin de plus de 32 bits de données d’instance, transmettez un pointeur vers une structure contenant les informations supplémentaires.

 

 
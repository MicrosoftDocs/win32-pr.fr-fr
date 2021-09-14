---
title: Macros et messages de fonctions MCI
description: Macros et messages de fonctions MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Messages MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195119"
---
# <a name="mci-functions-macros-and-messages"></a>Macros et messages de fonctions MCI

La plupart des applications MCI utilisent les fonctions [**mciSendString**](/previous-versions//dd757161(v=vs.85)) et [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) à des dizaines de fois. MCI fournit d’autres fonctions utiles que votre application utilisera moins fréquemment.

L’identificateur d’appareil requis par la plupart des commandes MCI est généralement récupéré dans un appel à la commande [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Si vous avez besoin d’un identificateur de périphérique mais que vous ne souhaitez pas ouvrir l’appareil, par exemple, si vous souhaitez interroger les fonctionnalités de l’appareil avant d’effectuer une autre action, vous pouvez appeler la fonction [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .

La fonction [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) permet à votre application d’utiliser un identificateur d’appareil pour récupérer un handle vers la tâche qui a créé cet identificateur.

Vous pouvez utiliser les fonctions [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) et [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) pour assigner et récupérer l’adresse de la fonction de rappel associée à l’indicateur d’attente (MCI \_ ).

La fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) récupère une chaîne qui décrit une valeur d’erreur MCI. Chaque chaîne renvoyée par MCI, qu’il s’agisse de données ou d’une description d’erreur, ne doit pas dépasser 128 caractères. Les champs de boîte de dialogue dont la taille est inférieure à 128 caractères tronquent les chaînes plus longues retournées par MCI. Pour plus d’informations sur ces chaînes, consultez [valeurs de retour de MCIERR](mcierr-return-values.md).

Les macros MCI sont des outils que vous pouvez utiliser pour créer et désassembler des valeurs qui spécifient des formats d’heure. Ces formats d’heure sont utilisés dans de nombreuses commandes MCI. Les formats traités par les macros sont heures/minutes/secondes (HMS), minutes/secondes/frames (MSF), et pistes/minutes/secondes/frames (TMSF). Le tableau suivant répertorie les macros et leurs descriptions.



| Macro                                        | Description                                        |
|----------------------------------------------|----------------------------------------------------|
| [**HMS de l' \_ \_ heure MCI**](mci-hms-hour.md)       | Récupère le composant hours à partir d’une valeur HMS.   |
| [**HMS de MCI \_ \_**](mci-hms-minute.md)   | Récupère le composant « minutes » à partir d’une valeur HMS. |
| [**MCI \_ HMS \_ seconde**](mci-hms-second.md)   | Récupère le composant « secondes » d’une valeur HMS. |
| [**MCI \_ Make \_ HMS**](mci-make-hms.md)       | Crée une valeur HMS.                              |
| [**MCI \_ Make \_ MSF**](mci-make-msf.md)       | Crée une valeur MSF.                              |
| [**MCI \_ Make \_ TMSF**](mci-make-tmsf.md)     | Crée une valeur TMSF.                              |
| [**\_cadre MSF de MCI \_**](/previous-versions//dd743438(v=vs.85))     | Récupère le composant frames à partir d’une valeur MSF.  |
| [**MCI \_ MSF \_ minute**](mci-msf-minute.md)   | Récupère le composant « minutes » à partir d’une valeur MSF. |
| [**MCI \_ MSF \_ second**](mci-msf-second.md)   | Récupère le composant « secondes » d’une valeur MSF. |
| [**\_Frame MCI TMSF \_**](mci-tmsf-frame.md)   | Récupère le composant frames à partir d’une valeur TMSF.  |
| [**TMSF de MCI \_ \_**](mci-tmsf-minute.md) | Récupère le composant « minutes » à partir d’une valeur TMSF. |
| [**MCI \_ TMSF \_ seconde**](mci-tmsf-second.md) | Récupère le composant « secondes » d’une valeur TMSF. |
| [**\_piste MCI TMSF \_**](mci-tmsf-track.md)   | Récupère le composant Tracks à partir d’une valeur TMSF.  |



 

MCI fournit également deux messages : [**mm \_ MCINOTIFY**](mm-mcinotify.md) et [**mm \_ MCISIGNAL**](mm-mcisignal.md). Le \_ message mm MCINOTIFY avertit une application du résultat d’une commande MCI chaque fois que cette commande spécifie l’indicateur « Notify » ( \_ notification MCI). Le \_ message MCISIGNAL mm est spécifique aux périphériques vidéo numériques ; il avertit l’application quand une position spécifiée est atteinte.

 

 
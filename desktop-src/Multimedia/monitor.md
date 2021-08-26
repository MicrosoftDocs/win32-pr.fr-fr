---
title: commande Monitor
description: La commande Monitor spécifie la source de la présentation. (La source de présentation par défaut est l’espace de travail.) Le fait de basculer la source de présentation change tous les flux audio et vidéo dans la source. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- commande monitor Windows multimédia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef9a47db68856196dc84aefb3c5f110941189dec80f62b369eae13c60932d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038809"
---
# <a name="monitor-command"></a>commande Monitor

La commande Monitor spécifie la source de la présentation. (La source de présentation par défaut est l’espace de travail.) Le fait de basculer la source de présentation change tous les flux audio et vidéo dans la source. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Un ou plusieurs des indicateurs suivants.



| Valeur           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fichier            | Spécifie que l’espace de travail est la source de présentation. Il s’agit de la source par défaut.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| entrée           | Spécifie que l’entrée externe est la source de la présentation. Si une commande de [lecture](play.md) est en cours, elle est d’abord suspendue. Si [setvideo](setvideo.md) a la valeur on, cet indicateur affiche une fenêtre masquée par défaut. Les appareils peuvent limiter ce que d’autres instances de périphérique peuvent faire lors de l’analyse de l’entrée.                                                                                                                                                                                                                                                                                                                                                                    |
| méthode *de méthode* | Lorsqu’il est utilisé avec **Monitor** « Input », cet indicateur sélectionne la méthode de surveillance. La *méthode* est « pre », « poster » ou « direct ». La surveillance directe demande que l’appareil soit configuré pour une qualité d’affichage optimale pendant la surveillance. La méthode de surveillance directe peut être incompatible avec l’enregistrement vidéo motion. La pré-surveillance et la postérieure à la surveillance autorisent l’enregistrement vidéo. La pré-surveillance affiche l’entrée externe avant la compression, tandis que le suivi de la surveillance affiche l’entrée externe après compression. En règle générale, différentes méthodes d’analyse ont des implications matérielles différentes. La méthode d’analyse par défaut est sélectionnée par l’appareil.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

La source de la présentation bascule automatiquement vers l’espace de travail après une commande [Play](play.md), [Step](step.md), [Pause](pause.md), [CUE](cue.md) « Output » ou [Seek](seek.md) . La commande d' [enregistrement](record.md) ne change pas automatiquement les sources de présentation, ce qui permet à votre application de ne pas afficher de vidéo lors de son enregistrement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[signal](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[répétition](play.md)
</dt> <dt>

[enregistrement](record.md)
</dt> <dt>

[Demandez](seek.md)
</dt> <dt>

[première](step.md)
</dt> </dl>

 


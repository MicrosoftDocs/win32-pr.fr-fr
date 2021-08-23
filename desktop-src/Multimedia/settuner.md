---
title: commande settuner
description: La commande settuner modifie le tuner actuel ou le paramètre de canal du tuner actuel. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- commande settuner Windows multimédia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7075de6ed50c49773a502ba77e093d84e85b079a6b17c462ea8ee65ad1330aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688797"
---
# <a name="settuner-command"></a>commande settuner

La commande settuner modifie le tuner actuel ou le paramètre de canal du tuner actuel. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Un des indicateurs suivants.



| Valeur                            | Signification                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *canal* de canal                | Définit le tuner sur le *canal*. Il se peut que vous ne puissiez pas modifier le canal pendant l’enregistrement, en fonction du magnétoscope. Un canal supérieur au maximum définit le tuner sur le canal maximal.                                                                                                                    |
| recherche de canal vers le canal vers le dessous | Recherche le canal suivant avec un signal valide. « Rechercher » incrémente le numéro de canal dans sa recherche. « Rechercher » décrémente le numéro de canal dans sa recherche. Le tuner est encapsulé dans Channel 1 lorsque le nombre maximal de canaux est dépassé. De même, lors de la recherche, le tuner revient au canal maximal. |
| canal vers le canal vers le PG.           | Incrémente ou décrémente le canal du tuner. Il se peut que vous ne puissiez pas modifier le canal pendant l’enregistrement, en fonction du magnétoscope. Le tuner est encapsulé dans Channel 1 lorsque le nombre maximal de canaux est dépassé. De même, lors de la recherche, le tuner revient au canal maximal.                              |
| nombre                   | Spécifie le tuner à affecter par la commande settuner. Si le *nombre* n’est pas donné, la valeur par défaut de 1 est utilisée.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

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
</dt> </dl>

 


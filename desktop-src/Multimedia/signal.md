---
title: signal, commande
description: La commande signal identifie une position spécifiée dans l’espace de travail en envoyant à l’application un \_ message MCISIGNAL mm. Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- commande signal Windows multimédia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363983"
---
# <a name="signal-command"></a>signal, commande

La commande signal identifie une position spécifiée dans l’espace de travail en envoyant à l’application un message [ \_ MCISIGNAL mm](mm-mcisignal.md) . Les périphériques vidéo numériques reconnaissent cette commande. MCIAVI ne prend en charge qu’un seul signal actif à la fois.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Un des indicateurs suivants.



| Valeur            | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| à la position      | Spécifie le frame pour appeler un signal.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| annuler           | Supprime les signaux de l’espace de travail. Un signal individuel est spécifié à l’aide de l’indicateur « uservalue ». Si l’indicateur « uservalue » n’est pas spécifié à l’aide de « Cancel », l’appareil annule tous les signaux. L’indicateur « Cancel » est incompatible avec les indicateurs « at », « Every » et « Return position ».                                                                                                                                                                                                                                                                                          |
| tous les *intervalles* | Spécifie la période des signaux. La valeur d' *intervalle* est spécifiée dans le format d’heure actuel. S’il est utilisé avec la *position*« at », les signaux sont placés dans l’espace de travail avec une marque de signal placée à la *position*.<br/> Sans l’indicateur « at », les signaux sont placés dans l’espace de travail avec un signal à la position actuelle.<br/> Si cet indicateur est omis, seule la position indiquée par l’indicateur « at » est marquée.<br/> Si la valeur d' *intervalle* est inférieure à la fréquence minimale prise en charge par un appareil, elle utilise sa valeur minimale.<br/> |
| position de retour  | Indique que l’appareil doit envoyer la valeur de position au lieu de l’identificateur « uservalue » dans le message de signalisation. L’identificateur « uservalue » peut toujours être utilisé pour annuler ou redéfinir les marques signalées.                                                                                                                                                                                                                                                                                                                                                                      |
| *ID* uservalue   | Spécifie un identificateur qui est renvoyé avec le message de signalisation. Cet identificateur agit comme un identificateur qui peut être utilisé avec d’autres commandes de **signal** pour faire référence à ce paramètre de **signal** . En cas d’omission, la valeur par défaut est zéro.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Le handle de fenêtre utilisé pour la notification des messages de saisie semi-automatique de commande est également utilisé pour la signalisation.

## <a name="requirements"></a>Spécifications



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

[\_MCISIGNAL mm](mm-mcisignal.md)
</dt> </dl>

 


---
title: Commande MCI_INDEX (mmsystem. h)
description: La \_ commande d’index MCI active ou désactive l’affichage à l’écran. Les périphériques VCR reconnaissent cette commande.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- commande MCI_INDEX Windows multimédia
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8e867098438a9df0be03646d85ff33fe857b285d0fda2763a3cecd46075f8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039209"
---
# <a name="mci_index-command"></a>\_Commande d’index MCI

La \_ commande d’index MCI active ou désactive l’affichage à l’écran. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificateur de l’appareil MCI qui doit recevoir le message de commande.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, MCI \_ Wait ou MCI \_ test. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les informations présentées dans l’affichage à l’écran sont contrôlées par l' \_ indicateur de jeu d’index magnétoscope MCI \_ \_ dans la commande [ \_ Set MCI](mci-set.md) .

Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :

<dl> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Désactive l’affichage à l’écran.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Active l’affichage à l’écran.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 


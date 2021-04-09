---
title: Commande MCI_SETTUNER (mmsystem. h)
description: La \_ commande MCI SETTUNER définit le canal actuel sur le tuner. Les périphériques VCR reconnaissent cette commande.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Commande MCI_SETTUNER Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033237"
---
# <a name="mci_settuner-command"></a>\_Commande MCI SETTUNER

La \_ commande MCI SETTUNER définit le canal actuel sur le tuner. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
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

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*
</dt> <dd>

Pointeur vers une [**structure \_ \_ SETTUNER \_ PARMS de magnétoscope MCI**](mci-vcr-settuner-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ canal SETTUNER magnétoscope \_ MCI
</dt> <dd>

Le membre **dwChannel** de la structure identifiée par *lpSetTuner* contient le nouveau numéro de canal.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_ \_ canal SETTUNER MCI \_ VCR \_
</dt> <dd>

Décrémente le canal du tuner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_SETTUNER de \_ canal \_ de \_ recherche \_ MCI VCR
</dt> <dd>

Recherche un canal valide dans le sens inverse.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_magnétoscope MCI \_ SETTUNER \_ canal de \_ recherche \_
</dt> <dd>

Recherche un canal valide dans la direction vers l’avant.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_ \_ canal SETTUNER MCI \_ VCR \_
</dt> <dd>

Incrémente le canal du tuner.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ numéro SETTUNER magnétoscope \_ MCI
</dt> <dd>

Le membre **dwNumber** de la structure identifiée par *lpSetTuner* spécifie le tuner logique à affecter avec cette commande.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 


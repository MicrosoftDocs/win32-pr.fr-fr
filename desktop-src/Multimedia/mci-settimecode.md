---
title: Commande MCI_SETTIMECODE (mmsystem. h)
description: La \_ commande MCI SETTIMECODE active ou désactive l’enregistrement du code temporel pour un magnétoscope. Les périphériques VCR reconnaissent cette commande.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- commande MCI_SETTIMECODE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363887"
---
# <a name="mci_settimecode-command"></a>\_Commande MCI SETTIMECODE

La \_ commande MCI SETTIMECODE active ou désactive l’enregistrement du code temporel pour un magnétoscope. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
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

<span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

L’indicateur supplémentaire suivant s’applique aux périphériques VCR :

<dl> <dt>

<span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_ \_ enregistrement SETTIMECODE magnétoscope \_ MCI
</dt> <dd>

Définit l’enregistrement du suivi du code temporel sur on ou OFF. Cet indicateur est utilisé en association avec l’un des indicateurs supplémentaires suivants :

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Enregistrement du code temporel sur.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Enregistrement du code temporel désactivé.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 


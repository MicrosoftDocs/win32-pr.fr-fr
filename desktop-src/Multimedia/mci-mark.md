---
title: Commande MCI_MARK (mmsystem. h)
description: La \_ commande de marque MCI enregistre ou efface les marques qui peuvent être utilisées avec la \_ commande MCI Seek pour les recherches à grande vitesse. Les périphériques VCR reconnaissent cette commande.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- Commande MCI_MARK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032551"
---
# <a name="mci_mark-command"></a>\_Commande MCI Mark

La \_ commande de marque MCI enregistre ou efface les marques qui peuvent être utilisées avec la commande [MCI \_ Seek](mci-seek.md) pour les recherches à grande vitesse. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
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

<span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants s’appliquent aux périphériques VCR :

<dl> <dt>

<span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_ \_ effacement des marques MCI magnétoscope \_
</dt> <dd>

Efface une marque à la position actuelle, si elle existe.

</dd> <dt>

<span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_écriture de \_ marquage \_ magnétoscope MCI
</dt> <dd>

Écrit une marque à la position actuelle.

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

 


---
title: Commande MCI_ESCAPE (mmsystem. h)
description: La \_ commande d’échappement MCI envoie une chaîne directement à l’appareil. Les appareils Videodisc reconnaissent cette commande.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- commande MCI_ESCAPE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195140"
---
# <a name="mci_escape-command"></a>\_Commande d’échappement MCI

La \_ commande d’échappement MCI envoie une chaîne directement à l’appareil. Les appareils Videodisc reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
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

\_Attente MCI Notify ou MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ échappement \_ MCI VD**](mci-vd-escape-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les données envoyées avec l' \_ échappement MCI sont dépendantes de l’appareil et sont généralement transmises directement au matériel associé à l’appareil.

L’indicateur supplémentaire suivant s’applique aux appareils videodisc :

<dl> <dt>

<span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_chaîne d' \_ échappement \_ VD MCI
</dt> <dd>

Une chaîne de commande est spécifiée dans le membre **lpstrCommand** de la structure identifiée par *lpEscape*. Cet indicateur est obligatoire.

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

 


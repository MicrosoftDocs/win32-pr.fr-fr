---
title: Commande MCI_PASTE (mmsystem. h)
description: La \_ commande de collage MCI colle les données du presse-papiers dans un fichier. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Commande MCI_PASTE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739828"
---
# <a name="mci_paste-command"></a>\_Commande de collage MCI

La \_ commande de collage MCI colle les données du presse-papiers dans un fichier. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Pointeur vers une structure [**MCI \_ DGV \_ coller \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>DGV MCI, \_ \_ coller \_ à l’adresse
</dt> <dd>

Un rectangle est inclus dans le membre **RC** de la structure identifiée par *lpPaste*. Les deux premières valeurs du rectangle spécifient le point dans le frame où placer les informations du presse-papiers. Si la hauteur et la largeur du rectangle sont différente de zéro, le contenu du presse-papiers est mis à l’échelle avec ces dimensions lorsqu’elles sont collées dans le cadre. Si l’indicateur est omis, MCI \_ colle par défaut le rectangle de cadre entier.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ coller \_ un \_ flux audio
</dt> <dd>

Un numéro de flux audio est inclus dans le membre **dwAudioStream** de la structure identifiée par *lpPaste*. S’il n’existe qu’un seul flux audio dans le presse-papiers, les données audio sont collées dans le flux désigné. Si plusieurs flux audio existent dans le presse-papiers, le flux indique le numéro de départ des séquences de flux. Si vous utilisez cet indicateur et que vous souhaitez également coller la vidéo, vous devez également utiliser \_ l' \_ indicateur MCI DGV coller la \_ vidéo \_ . (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés à partir du premier flux audio et vidéo. Chaque flux collé conserve son numéro de flux d’origine.)

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_DGV MCI \_ \_ Insérer
</dt> <dd>

Les données du presse-papiers doivent être insérées dans l’espace de travail existant à l’emplacement spécifié par l’MCI \_ pour l’indicateur. Toutes les données existantes après le point d’insertion sont déplacées dans l’espace de travail pour faire de la place. Il s’agit de la valeur par défaut.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>REMPLACEMENT de DGV MCI par le \_ \_ Collage \_
</dt> <dd>

Les données du presse-papiers doivent remplacer les données déjà présentes dans l’espace de travail. Les données de l’espace de travail remplacées suivent le point d’insertion.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_DGV MCI \_ coller \_ le \_ flux vidéo
</dt> <dd>

Un numéro de flux vidéo est inclus dans le membre **dwVideoStream** de la structure identifiée par *lpPaste*. S’il n’existe qu’un seul flux vidéo dans le presse-papiers, les données vidéo sont collées dans le flux désigné. Si plusieurs flux vidéo existent dans le presse-papiers, le flux indique le numéro de départ des séquences de flux. Si vous utilisez cet indicateur et que vous souhaitez également coller l’audio, vous devez également utiliser \_ l' \_ indicateur MCI DGV coller le \_ \_ flux audio. (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés à partir du premier flux audio et vidéo. Chaque flux collé conserve son numéro de flux d’origine.)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Une valeur position est incluse dans le membre **dwTo** de la structure identifiée par *lpPaste*. La valeur position spécifie la position à partir de laquelle commencer le collage des données dans l’espace de travail. Si cet indicateur est omis, la position par défaut correspond à la position actuelle.

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

 


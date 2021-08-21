---
title: Commande MCI_QUALITY (mmsystem. h)
description: La \_ commande MCI Quality définit un niveau de qualité personnalisé pour l’audio, la vidéo ou la compression des données d’image fixe. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- commande MCI_QUALITY Windows multimédia
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138220"
---
# <a name="mci_quality-command"></a>\_Commande de qualité MCI

La \_ commande MCI Quality définit un niveau de qualité personnalisé pour l’audio, la vidéo ou la compression des données d’image fixe. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ qualité \_ MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Le nom défini pour ce niveau de qualité peut être utilisé lors de la définition de l’audio, de la vidéo ou encore de la qualité avec les commandes [MCI \_ SETAUDIO](mci-setaudio.md) et [MCI \_ SETVIDEO](mci-setvideo.md) .

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ Quality \_ ALG
</dt> <dd>

Le membre **lpstrAlgorithm** de la structure identifiée par *lpQuality* contient l’adresse d’une mémoire tampon contenant le nom de l’algorithme. Cet algorithme doit être pris en charge par le pilote de périphérique et doit être compatible avec le descripteur audio, Persist ou Video utilisé. Si cet indicateur est omis, l’algorithme actuel est utilisé.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_boîte de \_ dialogue qualité MCI
</dt> <dd>

Le pilote de périphérique doit afficher une boîte de dialogue permettant de spécifier le niveau de qualité. La boîte de dialogue contient des champs spécifiques à l’algorithme utilisés en interne par le pilote de périphérique pour créer une structure décrivant un niveau de qualité spécifique.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_handle de qualité MCI \_
</dt> <dd>

Le membre **dwHandle** de la structure identifiée par *lpQuality* contient un handle vers une structure. La structure contient des données algorithmiques qui décrivent le niveau de qualité spécifique. Le format des structures pour les algorithmes dépend du périphérique.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_élément de qualité MCI \_
</dt> <dd>

Constante indiquant que le type d’algorithme est inclus dans le membre **dwItem** de la structure identifiée par *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>nom de la \_ qualité MCI \_
</dt> <dd>

Le membre **lpstrName** de la structure identifiée par *lpQuality* contient l’adresse d’une mémoire tampon contenant le descripteur de qualité.

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

 


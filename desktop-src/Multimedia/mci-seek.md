---
title: Commande MCI_SEEK (mmsystem. h)
description: La \_ commande MCI Seek change la position actuelle dans le contenu aussi rapidement que possible.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- commande MCI_SEEK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363852"
---
# <a name="mci_seek-command"></a>\_Commande MCI Seek

La \_ commande MCI Seek change la position actuelle dans le contenu aussi rapidement que possible. La sortie vidéo et audio est désactivée au cours de la recherche. Une fois la recherche terminée, l’appareil est arrêté. Les périphériques CD audio, Digital-Video, MIDI Sequencer, VCR, videodisc et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ recherche MCI**](mci-seek-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Si la taille de l’échantillon de données d’un appareil est supérieure à 1 octet (comme avec les données stéréo audio Wave), cette commande passe au début de l’échantillon le plus proche lorsqu’une position spécifiée ne coïncide pas avec le début d’un échantillon.

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Seek :

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>\_recherche MCI \_ à la \_ fin
</dt> <dd>

Recherchez la fin du contenu.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ Seek \_ to \_ Start
</dt> <dd>

Recherche jusqu’au début du contenu.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ vers
</dt> <dd>

Une position est incluse dans le membre **dwTo** de la structure identifiée par *lpSeek*. Les unités affectées aux valeurs de position sont spécifiées avec \_ l' \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) . N’utilisez pas cet indicateur avec MCI \_ Seek \_ to \_ end ou MCI \_ Seek \_ to \_ Start.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>\_magnétoscope \_ de recherche MCI \_ à
</dt> <dd>

Le membre **dwAt** de la structure identifiée par *lpSeek* contient une heure de début de la commande entière.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marque de \_ recherche MCI magnétoscope \_
</dt> <dd>

Le membre **dwMark** de la structure identifiée par *lpSeek* contient la marque numérotée à rechercher.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>l' \_ inverse de la recherche MCI magnétoscope \_ \_
</dt> <dd>

La direction de la recherche est inversée ; utilisé uniquement avec l' \_ indicateur de marque de recherche de magnétoscope MCI \_ \_ .

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpSeek* pointe vers une structure de [**\_ \_ recherche \_ de magnétoscope MCI**](mci-vcr-seek-parms.md) .

L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **videodisc** :

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>MCI \_ de \_ recherche \_ MCI
</dt> <dd>

La direction de la recherche est inversée.

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

 


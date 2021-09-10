---
title: Commande MCI_SAVE (mmsystem. h)
description: La \_ commande MCI Save enregistre le fichier actif.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- commande MCI_SAVE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363883"
---
# <a name="mci_save-command"></a>\_Commande d’enregistrement MCI

La \_ commande MCI Save enregistre le fichier actif. Les appareils qui modifient des fichiers ne doivent pas détruire la copie d’origine jusqu’à ce qu’ils reçoivent le message d’enregistrement. Les périphériques vidéo-superposition et Waveform-Audio reconnaissent cette commande. Bien que les périphériques vidéo numériques et les séquenceurs MIDI reconnaissent également cette commande, les pilotes MCIAVI et MCISEQ ne les implémentent pas.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ enregistrement MCI**](mci-save-parms.md) . (Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Cette commande est prise en charge par les appareils qui renvoient la **valeur true** lorsque vous appelez la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) avec l' \_ indicateur MCI GETDEVCAPS \_ CAN \_ Save.

L’indicateur supplémentaire suivant s’applique à tous les périphériques prenant en charge [MCI \_ Save](/windows):

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_fichier d’enregistrement MCI \_
</dt> <dd>

Le membre **lpFileName** de la structure identifiée par *lpSave* contient l’adresse d’une mémoire tampon contenant le nom de fichier de destination.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpSave* contient un rectangle valide. Le rectangle spécifie une région de la mémoire tampon de trame qui sera enregistrée dans le fichier spécifié. La première paire de coordonnées spécifie l’angle supérieur gauche du rectangle. la deuxième paire spécifie la largeur et la hauteur. Les périphériques vidéo numériques doivent utiliser la commande [MCI \_ capture](mci-capture.md) pour capturer le contenu de la mémoire tampon de trame. (Les périphériques de superposition vidéo doivent également utiliser MCI \_ CAPTURE.) Cet indicateur est destiné à la compatibilité avec le jeu de commandes de superposition vidéo MCI existant.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_enregistrement d' \_ \_ abandon DGV MCI
</dt> <dd>

Arrête une opération d’enregistrement en cours. Il doit s’agir du seul indicateur présent.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>\_enregistrement DGV \_ MCI \_ KEEPRESERVE
</dt> <dd>

L’espace disque restant inutilisé par rapport à la commande de [ \_ réserve MCI](mci-reserve.md) d’origine n’est pas libéré.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpSave* pointe vers une structure [**MCI \_ DGV \_ Save \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .

L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpSave* contient un rectangle d’affichage valide indiquant la zone de la mémoire tampon vidéo à enregistrer.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpSave* pointe vers une structure [**MCI \_ OVLY \_ Save \_ PARMS**](/previous-versions//dd743447(v=vs.85)) .

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

 


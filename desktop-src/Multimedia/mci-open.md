---
title: Commande MCI_OPEN (mmsystem. h)
description: La \_ commande Open MCI Initialise un appareil ou un fichier. Tous les appareils reconnaissent cette commande.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Commande MCI_OPEN Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843045"
---
# <a name="mci_open-command"></a>\_Commande d’ouverture MCI

La \_ commande Open MCI Initialise un appareil ou un fichier. Tous les appareils reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Pointeur désignant une structure de [**\_ \_ PARMS ouverte avec MCI**](mci-open-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

L' \_ indicateur de \_ type Open MCI doit être utilisé chaque fois qu’un appareil est spécifié dans la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Si vous ouvrez un appareil en spécifiant une constante de type d’appareil, vous devez spécifier \_ l' \_ indicateur MCI Open type \_ ID en plus du \_ type MCI Open \_ . Pour obtenir la liste des constantes de type d’appareil, consultez [types d’appareils MCI](mci-device-types.md).

Si l' \_ indicateur de \_ partage ouvert MCI n’est pas spécifié lors de l’ouverture initiale d’un appareil ou d’un fichier, toutes les commandes Open MCI ultérieures \_ à l’appareil ou au fichier échoueront. Si l’appareil ou le fichier est déjà ouvert et que cet indicateur n’est pas spécifié, l’appel échoue même si la première commande ouverte a spécifié le \_ partage MCI ouvert \_ . Fichiers ouverts pour MCISEQ. DRV et MCIWAVE. Les appareils DRV ne peuvent pas être partagés.

La casse est ignorée dans le nom de l’appareil, mais il ne peut pas y avoir de espaces à gauche ou à droite.

Pour utiliser la sélection automatique de type (via les entrées du registre), affectez le nom de fichier et l’extension de fichier au membre **lpstrElementName** de la structure identifiée par *lpOpen*, affectez la valeur **null** au membre **lpstrDeviceType** et définissez l' \_ indicateur d’élément Open MCI \_ .

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils prenant en charge MCI \_ Open :

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias d’ouverture MCI \_
</dt> <dd>

Un alias est inclus dans le membre **lpstrAlias** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>\_ouvrir un \_ partage MCI
</dt> <dd>

L’appareil ou le fichier doit être ouvert comme partageable.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>\_type d’ouverture MCI \_
</dt> <dd>

Un nom ou une constante de type d’appareil est inclus dans le membre **lpstrDeviceType** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ID de \_ type d’ouverture MCI \_
</dt> <dd>

Le mot de poids faible du membre **lpstrDeviceType** de la structure identifiée par *lpOpen* contient un identificateur de type d’appareil MCI standard et le mot de poids fort peut éventuellement contenir l’index ordinal de l’appareil. Utilisez cet indicateur avec l' \_ indicateur de \_ type Open MCI.

</dd> </dl>

Les indicateurs supplémentaires suivants s’appliquent aux appareils composés :

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>MCI \_ Open ( \_ élément)
</dt> <dd>

Un nom de fichier est inclus dans le membre **lpstrElementName** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ID d' \_ élément \_ Open MCI
</dt> <dd>

Le membre **lpstrElementName** de la structure identifiée par *lpOpen* est interprété comme une valeur **DWORD** et a une signification interne à l’appareil. Utilisez cet indicateur avec l' \_ indicateur d' \_ élément Open MCI.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ ouvrir \_ nostatic
</dt> <dd>

L’appareil doit réduire le nombre de couleurs (système) statiques dans la palette. Cela augmente le nombre de couleurs disponibles pour le rendu du flux vidéo. Cet indicateur s’applique uniquement aux appareils qui partagent une palette avec Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>\_DGV \_ Open \_ parent de MCI
</dt> <dd>

Le handle de la fenêtre parente est spécifié dans le membre **hwndParent** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ Open \_ WS
</dt> <dd>

Un style de fenêtre est spécifié dans le membre **dwStyle** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ ouvrir le \_ 16 bits
</dt> <dd>

Indique une préférence pour la prise en charge des appareils MCI 16 bits.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ Open \_ 32 bits
</dt> <dd>

Indique une préférence pour la prise en charge des appareils MCI 32 bits.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpOpen* pointe vers une structure [**MCI \_ DGV \_ Open \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>\_OVLY \_ Open \_ parent de MCI
</dt> <dd>

Le handle de la fenêtre parente est spécifié dans le membre **hwndParent** de la structure identifiée par *lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ Open \_ WS
</dt> <dd>

Un style de fenêtre est spécifié dans le membre **dwStyle** de la structure identifiée par *lpOpen*. La valeur **dwStyle** spécifie le style de la fenêtre que le pilote créera et affichera si l’application n’en fournit pas. Le paramètre style prend un entier qui définit le style de la fenêtre. Ces constantes sont les mêmes que les styles de fenêtre standard (tels que WS \_ Child, WS \_ OVERLAPPEDWINDOW ou WS \_ popup).

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpOpen* pointe vers une structure de paramètres d' [**ouverture (MCI \_ OVLY \_ Open \_ PARMS**](mci-ovly-open-parms.md) ).

L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_tampon d' \_ ouverture MCI Wave \_
</dt> <dd>

Une longueur de tampon est spécifiée dans le membre **dwBufferSeconds** de la structure identifiée par *lpOpen*.

</dd> </dl>

Pour les périphériques audio Waveform, le paramètre *lpOpen* pointe vers une structure de paramètres d’ouverture de l' [**\_ onde \_ \_ MCI**](mci-wave-open-parms.md) . Le pilote MCIWAVE requiert un périphérique audio Wave asynchrone.

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

 


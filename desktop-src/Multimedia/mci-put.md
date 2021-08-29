---
title: Commande MCI_PUT (mmsystem. h)
description: La \_ commande MCI put définit les rectangles de la source, de la destination et du frame. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- commande MCI_PUT Windows multimédia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c34250f59122eca942309b840c4b66521a08b3eecc8ca89dfd480d6e9a6869d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689909"
---
# <a name="mci_put-command"></a>\_Commande put MCI

La \_ commande MCI put définit les rectangles de la source, de la destination et du frame. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques, test MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_client MCI DGV \_ put \_
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ Rect s’applique à la position de la fenêtre cliente. Le rectangle spécifié est relatif à la fenêtre parente de la fenêtre d’affichage. \_ \_ La fenêtre put DGV MCI \_ doit être définie simultanément avec cet indicateur.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>DGV de mise en place de la \_ \_ \_ destination MCI
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ rect spécifie un rectangle de destination. Le rectangle de destination spécifie la partie de la fenêtre cliente associée à cette instance de pilote de périphérique qui affiche l’image ou la vidéo.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_ \_ image put DGV \_ MCI
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ Rect s’applique au rectangle de cadre. Le rectangle de frame spécifie la partie de la mémoire tampon de trame utilisée comme destination des images vidéo obtenues à partir du rectangle vidéo. La vidéo doit être mise à l’échelle pour s’ajuster au rectangle de la mémoire tampon de trame.

Le rectangle est spécifié dans les coordonnées de la mémoire tampon de trame. Le rectangle par défaut est la mémoire tampon d’image complète. La spécification de ce rectangle permet à l’appareil de mettre l’image à l’échelle au fur et à mesure qu’elle numérise les données. Les appareils qui ne peuvent pas mettre à l’échelle l’image rejettent cette commande avec une \_ fonction non prise en charge par MCIERR \_ . Vous pouvez utiliser l' \_ indicateur MCI GETDEVCAPS \_ peut \_ Stretch avec la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) pour déterminer si un appareil met à l’échelle l’image. Un appareil retourne la **valeur false** s’il ne peut pas mettre l’image à l’échelle.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_source MCI DGV \_ put \_
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ rect spécifie un rectangle source. Le rectangle source spécifie la partie de la mémoire tampon de trame à mettre à l’échelle pour s’ajuster au rectangle de destination.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_vidéo MCI DGV \_ put \_
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ Rect s’applique au rectangle vidéo. Le rectangle vidéo spécifie la partie de la source de présentation actuelle qui est stockée dans la mémoire tampon de trame. Le rectangle est spécifié à l’aide des coordonnées naturelles de la source de présentation. Il permet la spécification du rognage qui se produit avant de stocker des images et des vidéos dans le tampon de trame. Le rectangle par défaut est la zone de numérisation active complète ou les images et vidéos décompressées complètes.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ \_ fenêtre put DGV \_ MCI
</dt> <dd>

Le rectangle défini pour MCI \_ DGV \_ Rect s’applique à la fenêtre d’affichage. Ce rectangle est relatif à la fenêtre parente de la fenêtre d’affichage (généralement le bureau). Si la fenêtre n’est pas spécifiée, la taille et la position de la fenêtre initiale sont définies par défaut.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpDest* contient un rectangle valide.

</dd> </dl>

Pour les périphériques vidéo numériques, *lpDest* pointe vers une structure [**MCI \_ DGV \_ put \_ PARMS**](/previous-versions//dd743397(v=vs.85)) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>OVLY de mise en place de la \_ \_ \_ destination MCI
</dt> <dd>

Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la fenêtre cliente utilisée pour afficher une image. Le rectangle contient le décalage et l’étendue visible de l’image par rapport à l’origine de la fenêtre. Si le frame est étiré, la source est étirée sur le rectangle de destination.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_ \_ image put OVLY \_ MCI
</dt> <dd>

Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la mémoire tampon vidéo utilisée pour recevoir l’image vidéo. Le rectangle contient le décalage et l’étendue de la zone de mémoire tampon par rapport à l’origine de la mémoire tampon vidéo.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_source MCI OVLY \_ put \_
</dt> <dd>

Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la mémoire tampon vidéo utilisée comme source de l’image numérique. Le rectangle contient le décalage et l’étendue du rectangle de découpage pour la mémoire tampon vidéo par rapport à son origine.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_vidéo MCI OVLY \_ put \_
</dt> <dd>

Le rectangle défini pour MCI \_ OVLY \_ rect spécifie la zone de la capture de la source vidéo par la mémoire tampon vidéo. Le rectangle contient le décalage et l’étendue du rectangle de découpage pour la source vidéo par rapport à son origine.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpDest* contient un rectangle d’affichage valide. Si cet indicateur n’est pas spécifié, le rectangle par défaut correspond aux coordonnées du tampon vidéo ou de la fenêtre qui est découpée.

</dd> </dl>

Pour les périphériques de superposition vidéo, *lpDest* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .

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

 


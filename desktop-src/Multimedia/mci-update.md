---
title: Commande MCI_UPDATE (mmsystem. h)
description: La \_ commande de mise à jour MCI met à jour le rectangle d’affichage. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- commande MCI_UPDATE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58333b108891a8bcd0e0548d4dcd0db2f2606d1259f0934f19b8f6804afab3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689679"
---
# <a name="mci_update-command"></a>\_Commande de mise à jour MCI

La \_ commande de mise à jour MCI met à jour le rectangle d’affichage. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
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

**MCI \_ NOTIFY**, **MCI \_ Wait** ou, pour les périphériques vidéo numériques, **\_ test MCI**. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « Digitalvideo » :

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI \_ DGV \_ mise à jour \_ HDC
</dt> <dd>

Le membre **HDC** de la structure identifiée par *lpDest* contient une fenêtre valide du contrôleur de contenu à peindre. Cet indicateur est obligatoire.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide. Le rectangle spécifie le rectangle de découpage par rapport au rectangle client.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_ \_ mise à jour de MCI DGV \_
</dt> <dd>

Une application utilise cet indicateur lorsqu’elle reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) destiné à un contrôleur de périphérique d’affichage. En général, un périphérique de mémoire tampon de trame peint la couleur de la clé. Si le périphérique d’affichage n’a pas de mémoire tampon de trame, il est possible qu’il ignore la \_ commande de mise à jour de MCI lorsque l’indicateur de **\_ peinture MCI DGV \_ \_ Update** est utilisé, car l’affichage est repeint au cours de l’opération de lecture.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpDest* pointe vers une structure de [**\_ \_ mise \_ à jour MCI DGV**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .

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

 


---
title: Commande MCI_WHERE (mmsystem. h)
description: La \_ commande MCI qui obtient le rectangle de découpage du périphérique vidéo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Commande MCI_WHERE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942186"
---
# <a name="mci_where-command"></a>\_Commande MCI Where

La \_ commande MCI qui obtient le rectangle de découpage du périphérique vidéo. Les appareils vidéo et vidéo numériques reconnaissent cette commande. Les membres **supérieur** et **gauche** du [Rect](/previous-versions//ms536136(v=vs.85)) retourné contiennent l’origine du rectangle de découpage, et les membres de **droite** et du **bas** contiennent la largeur et la hauteur du rectangle de découpage. (Il ne s’agit pas de l’utilisation standard des membres **droits** et **inférieurs** .)

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>\_DGV MCI \_ où \_ destination
</dt> <dd>

Obtient une description de la zone rectangulaire utilisée pour afficher la vidéo et les images dans la zone cliente de la fenêtre active.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV \_ où \_ Frame
</dt> <dd>

Obtient une description de la zone rectangulaire de la mémoire tampon de trame dans laquelle les images du rectangle vidéo sont mises à l’échelle. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>DGV MCI, \_ \_ où \_ Max
</dt> <dd>

En cas d’utilisation avec MCI \_ DGV \_ où \_ destination ou MCI \_ DGV \_ où \_ source, le rectangle retourné indique la largeur et la hauteur maximales de la région spécifiée. Lorsqu’il est utilisé avec MCI \_ DGV \_ \_ , le rectangle retourné indique la taille de l’affichage entier.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ où \_ source
</dt> <dd>

Obtient une description de la zone rectangulaire (rognée de la mémoire tampon de frame) qui est étirée pour s’ajuster au rectangle de destination sur l’affichage.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ DGV \_ où \_ vidéo
</dt> <dd>

Obtient une description de la zone rectangulaire rognée de la source de présentation pour remplir le rectangle de cadre dans la mémoire tampon de frame. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ où \_ fenêtre
</dt> <dd>

Obtient une description du frame de fenêtre d’affichage.

</dd> <dt>


</dt> <dd></dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpQuery* pointe vers un **MCI \_ DGV \_ où \_** la structure PARMS. La structure **MCI \_ DGV \_ où \_ parms** est identique à la structure [**MCI \_ DGV \_ rect \_ parms**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>\_OVLY MCI \_ où \_ destination
</dt> <dd>

Obtient le rectangle d’affichage de la destination. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY \_ où \_ Frame
</dt> <dd>

Obtient le rectangle de frame de superposition. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ où \_ source
</dt> <dd>

Obtient le rectangle source. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ où \_ vidéo
</dt> <dd>

Obtient le rectangle vidéo. Les coordonnées des rectangles sont placées dans le membre **RC** de la structure identifiée par *lpQuery*.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpQuery* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .

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

 


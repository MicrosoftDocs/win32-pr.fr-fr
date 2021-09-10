---
title: Commande MCI_WINDOW (mmsystem. h)
description: La \_ commande de fenêtre MCI spécifie la fenêtre et les caractéristiques de la fenêtre pour les périphériques graphiques. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- commande MCI_WINDOW Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363871"
---
# <a name="mci_window-command"></a>\_Commande de fenêtre MCI

La \_ commande de fenêtre MCI spécifie la fenêtre et les caractéristiques de la fenêtre pour les périphériques graphiques. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les appareils graphiques doivent créer une fenêtre par défaut lorsqu’un appareil est ouvert, mais ne doivent pas l’afficher tant qu’ils n’ont pas reçu la commande [MCI \_ Play](mci-play.md) . La \_ commande de fenêtre MCI est utilisée pour fournir une fenêtre créée par l’application à l’appareil et pour modifier les caractéristiques d’affichage d’une fenêtre d’affichage définie par l’application ou par défaut. Si l’application fournit la fenêtre d’affichage, vous devez préparer la mise à jour d’un rectangle non valide dans la fenêtre.

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_HWND de \_ fenêtre \_ DGV MCI
</dt> <dd>

Le descripteur de la fenêtre nécessaire pour une utilisation comme destination est inclus dans le membre **HWND** de la structure identifiée par *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>État de la \_ fenêtre DGV MCI \_ \_
</dt> <dd>

Le membre **nCmdShow** de la structure identifiée par *lpWindow* contient des paramètres pour définir l’état de la fenêtre.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>texte de la \_ fenêtre DGV MCI \_ \_
</dt> <dd>

Le membre **lpstrText** de la structure identifiée par *lpWindow* contient l’adresse d’une mémoire tampon contenant la légende utilisée dans la barre de titre de la fenêtre.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpWindow* pointe vers une structure de [**\_ \_ fenêtre \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>\_fenêtre OVLY \_ MCI \_ désactiver \_ Stretch
</dt> <dd>

Désactive l’étirement de l’image.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_fenêtre OVLY \_ MCI \_ activer \_ Stretch
</dt> <dd>

Active l’étirement de l’image.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_HWND de \_ fenêtre \_ OVLY MCI
</dt> <dd>

Le descripteur de la fenêtre utilisée pour la destination est inclus dans le membre **HWND** de la structure identifiée par *lpWindow*. Définissez cet indicateur sur MCI \_ OVLY \_ \_ par défaut pour revenir à la fenêtre par défaut.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>État de la \_ fenêtre OVLY MCI \_ \_
</dt> <dd>

Le membre **nCmdShow** de la structure *lpWindow* contient des paramètres pour définir l’état de la fenêtre. Cet indicateur revient à appeler [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) avec le paramètre *State* . Les constantes sont les mêmes que celles définies dans les fenêtres. H (tels que SW \_ Hide, SW \_ Minimize ou SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>texte de la \_ fenêtre OVLY MCI \_ \_
</dt> <dd>

Le membre **lpstrText** de la structure identifiée par *lpWindow* contient l’adresse d’une mémoire tampon contenant la légende utilisée pour la fenêtre.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpWindow* pointe vers une structure de fenêtre d’affichage [**MCI \_ OVLY \_ \_**](mci-ovly-window-parms.md) .

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

 


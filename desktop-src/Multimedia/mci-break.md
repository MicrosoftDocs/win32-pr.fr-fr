---
title: Commande MCI_BREAK (mmsystem. h)
description: La \_ commande MCI Break définit une clé d’arrêt pour un appareil MCI. MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil. Toute application MCI peut utiliser cette commande.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- commande MCI_BREAK Windows multimédia
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119617"
---
# <a name="mci_break-command"></a>\_Commande MCI Break

La \_ commande MCI Break définit une clé d’arrêt pour un appareil MCI. MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil. Toute application MCI peut utiliser cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils Digital-Video et Video-cassette Recorder (magnétoscope), \_ test MCI. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ sauts MCI**](mci-break-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Vous devrez peut-être appuyer plusieurs fois sur la touche pause pour interrompre une opération d’attente. Le fait d’appuyer sur la touche Attn après l’annulation d’un appareil peut envoyer la pause à une application. Si une application a une action définie pour le code de clé virtuelle, elle peut répondre par inadvertance à l’arrêt. Par exemple, une application utilisant VK \_ Annuler pour une touche accélérateur peut répondre à la touche CTRL + ATTN par défaut si elle est appuyée après l’annulation d’une attente.

Les indicateurs supplémentaires suivants s’appliquent à tous les appareils :

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND de pause MCI \_
</dt> <dd>

Le membre **hwndBreak** de la structure identifiée par *lpBreak* contient un handle de fenêtre qui doit être la fenêtre active afin d’activer la détection de rupture pour ce périphérique MCI. Il s’agit généralement de la fenêtre principale de l’application. En cas d’omission, MCI ne vérifie pas le handle de fenêtre de la fenêtre active.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_touche pause \_ MCI
</dt> <dd>

Le membre **nVirtKey** de la structure identifiée par *lpBreak* spécifie le code de touche virtuelle utilisé pour la touche Attn. Par défaut, MCI attribue la touche d’arrêt CTRL + ATTN. Cet indicateur est requis si la \_ \_ déconnexion MCI n’est pas spécifiée.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>\_Pause MCI \_
</dt> <dd>

Désactive toute clé d’arrêt existante pour l’appareil indiqué.

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

 


---
title: Commande MCI_CAPTURE (mmsystem. h)
description: La \_ commande MCI capture capture le contenu de la mémoire tampon de trame et le stocke dans un fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- commande MCI_CAPTURE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041954d786b007023226fb5d3febf4747c0121e2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363767"
---
# <a name="mci_capture-command"></a>\_Commande de capture MCI

La \_ commande MCI capture capture le contenu de la mémoire tampon de trame et le stocke dans un fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
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

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Pointeur vers une structure de [**\_ DGV de \_ capture \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ capture \_ en tant que
</dt> <dd>

Le membre **lpstrFileName** de la structure identifiée par *lpCapture* contient l’adresse d’une mémoire tampon spécifiant le chemin d’accès et le nom de fichier de destination. (Cet indicateur est obligatoire.)

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>\_DGV \_ de la capture MCI \_ sur
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpCapture* contient un rectangle valide. Le rectangle spécifie la zone rectangulaire dans la mémoire tampon de trame qui est rognée et enregistrée sur le disque. En cas d’omission, la zone rognée est définie par défaut sur le rectangle spécifié ou par défaut sur une commande [ \_ put précédente MCI](mci-put.md) qui spécifie la zone source pour cette instance du pilote de périphérique.

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

 


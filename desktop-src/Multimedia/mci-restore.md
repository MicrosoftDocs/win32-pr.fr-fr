---
title: Commande MCI_RESTORE (mmsystem. h)
description: La \_ commande de restauration MCI copie une image bitmap d’un fichier vers la mémoire tampon de trame. Les périphériques vidéo numériques reconnaissent cette commande. Cette commande effectue l’action inverse de la \_ commande de capture MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Commande MCI_RESTORE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742812"
---
# <a name="mci_restore-command"></a>\_Commande de restauration MCI

La \_ commande de restauration MCI copie une image bitmap d’un fichier vers la mémoire tampon de trame. Les périphériques vidéo numériques reconnaissent cette commande. Cette commande effectue l’action inverse de la commande de [ \_ capture MCI](mci-capture.md) .

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

Pointeur vers une structure de [**\_ paramètres de \_ restauration \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

L’implémentation peut reconnaître un grand nombre de formats d’image, mais une image bitmap indépendante du périphérique (DIB) Windows est toujours acceptée.

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_ \_ restauration \_ à partir de MCI DGV
</dt> <dd>

Le membre **lpstrFileName** de la structure identifiée par *lpRestore* contient l’adresse d’une mémoire tampon contenant le nom du fichier source. Le nom de fichier est obligatoire.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_ \_ restauration de DGV MCI \_ sur
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpRestore* contient un rectangle valide. Le rectangle spécifie une région de la mémoire tampon de trame par rapport à son origine. La première paire de coordonnées spécifie l’angle supérieur gauche du rectangle. la deuxième paire spécifie la largeur et la hauteur. Si cet indicateur n’est pas spécifié, l’image est copiée dans l’angle supérieur gauche de la mémoire tampon de trame.

</dd> </dl>

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

 


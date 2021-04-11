---
title: Commande MCI_FREEZE (mmsystem. h)
description: La \_ commande MCI Freeze fige le mouvement à l’écran. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Commande MCI_FREEZE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032554"
---
# <a name="mci_freeze-command"></a>\_Commande de blocage MCI

La \_ commande MCI Freeze fige le mouvement à l’écran. Les appareils vidéo numérique, vidéo-superposition et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants sont utilisés par le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_ \_ blocage de DGV MCI \_ à
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpFreeze* contient un rectangle valide. Le rectangle spécifie une zone dans la mémoire tampon de trame dont le bit de masque de verrouillage est activé pour chaque pixel. Les pixels spécifiés ne sont pas mis à jour tant que le bit de masque de verrouillage n’est pas désactivé. Si cet indicateur n’est pas spécifié, le rectangle prend par défaut la totalité de la mémoire tampon de trame. Cet indicateur est pris en charge uniquement si la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) retourne la **valeur true** pour l' \_ indicateur de verrouillage MCI DGV \_ GETDEVCAPS \_ \_ .

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI \_ DGV \_ bloqué \_ en dehors
</dt> <dd>

La zone en dehors de la région spécifiée pour \_ l' \_ indicateur MCI DGV Freeze \_ est figée.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpFreeze* pointe vers une structure [**MCI \_ DGV \_ Freeze \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .

Les indicateurs supplémentaires suivants sont utilisés par le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_champ de \_ blocage du magnétoscope MCI \_
</dt> <dd>

Figer un seul membre du frame actuel.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_Frame de \_ blocage MCI VCR \_
</dt> <dd>

Figer les deux champs du frame actuel.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_ \_ entrée figer le magnétoscope MCI \_
</dt> <dd>

Fige le frame actuel sur l’écran (utilisé pour l’enregistrement).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_sortie de \_ blocage de magnétoscope MCI \_
</dt> <dd>

Figer le frame actuel à partir du magnétoscope (utilisé avec la capture de frame).

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpFreeze* pointe vers une structure de paramètres [**\_ génériques \_ MCI**](mci-generic-parms.md) .

L’indicateur supplémentaire suivant est utilisé par le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpFreeze* contient un rectangle valide. Si cet indicateur n’est pas spécifié, le pilote de périphérique gèle l’ensemble du frame.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpFreeze* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .

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

 


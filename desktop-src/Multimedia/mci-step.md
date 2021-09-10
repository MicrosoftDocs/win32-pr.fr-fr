---
title: Commande MCI_STEP (mmsystem. h)
description: La \_ commande d’étape MCI dénombre les frames d’un ou de plusieurs frames. Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- commande MCI_STEP Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363936"
---
# <a name="mci_step-command"></a>\_Commande d’étape MCI

La \_ commande d’étape MCI dénombre les frames d’un ou de plusieurs frames. Les appareils Digital-Video, VCR et CAV-format videodisc reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Cette commande prend en charge les appareils qui renvoient la **valeur true** à l' \_ GETDEVCAPS MCI \_ a \_ un indicateur vidéo de la commande [MCI \_ GETDEVCAPS](mci-getdevcaps.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ frames d’étape DGV MCI \_
</dt> <dd>

Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre d’images à avancer avant d’afficher une autre image.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>\_ \_ étape inverse DGV \_ MCI
</dt> <dd>

Étapes dans l’ordre inverse.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpStep* pointe vers une structure [**MCI \_ DGV \_ Step \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_ \_ images pas à pas de magnétoscope MCI \_
</dt> <dd>

Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre d’images à avancer avant d’afficher une autre image.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_étape de magnétoscope MCI \_ \_ inversée
</dt> <dd>

Étapes dans l’ordre inverse.

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpStep* pointe vers une structure d' [**\_ \_ étape \_ de magnétoscope MCI**](mci-vcr-step-parms.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** :

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_images d' \_ étape MCI VD \_
</dt> <dd>

Le membre **dwFrames** de la structure identifiée par *lpStep* spécifie le nombre de frames à exécuter pas à pas.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>étape de l’étape MCI MCI \_ \_ \_
</dt> <dd>

Étapes dans l’ordre inverse.

</dd> </dl>

Pour les appareils videodisc, le paramètre *lpStep* pointe vers une structure d’étape de la [**\_ \_ séquence \_ MCI**](mci-vd-step-parms.md) .

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

 


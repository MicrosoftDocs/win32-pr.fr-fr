---
title: Commande MCI_UNFREEZE (mmsystem. h)
description: La commande MCI dégeler \_ restaure le mouvement vers une zone de la mémoire tampon vidéo figée avec la \_ commande de blocage MCI. Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- commande MCI_UNFREEZE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195067"
---
# <a name="mci_unfreeze-command"></a>\_Commande MCI libérer

La commande MCI dégeler \_ restaure le mouvement vers une zone de la mémoire tampon vidéo figée avec la commande de [ \_ blocage MCI](mci-freeze.md) . Les périphériques numériques vidéo, VCR et vidéo reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

L’indicateur supplémentaire suivant est utilisé avec le type d’appareil **Digitalvideo** :

\_DGV MCI \_

Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide. Le rectangle spécifie une zone dans la mémoire tampon de trame dont le bit de masque de verrouillage doit être désactivé sur les pixels. Les régions rectangulaires sont spécifiées comme décrit pour la commande [ \_ put MCI](mci-put.md) . En cas d’omission, le rectangle a comme valeur par défaut la mémoire tampon de frame entière. En utilisant une séquence de commandes figer et dégeler avec différents rectangles, des modèles arbitraires de bits de masque de verrouillage peuvent être décrits.

Pour les périphériques vidéo numériques, le paramètre *lpUnfreeze* pointe vers une structure **MCI \_ DGV \_ dégeler \_** . Pour plus d’informations, consultez les commentaires relatifs à la structure [**MCI \_ DGV \_ rect \_ PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>entrée de l’entrée de \_ magnétoscope MCI \_ \_
</dt> <dd>

Libérez l’entrée.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_sortie du magnétoscope MCI \_ \_
</dt> <dd>

Libérez la sortie.

</dd> </dl>

L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpUnfreeze* contient un rectangle d’affichage valide. Il s’agit d’un paramètre obligatoire.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpUnfreeze* pointe vers une structure [**MCI \_ OVLY \_ rect \_ PARMS**](mci-ovly-rect-parms.md) .

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

 


---
title: Commande MCI_LOAD (mmsystem. h)
description: La \_ commande de chargement MCI charge un fichier. Les appareils vidéo et vidéo numériques reconnaissent cette commande.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- commande MCI_LOAD Windows multimédia
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363831"
---
# <a name="mci_load-command"></a>\_Commande de chargement MCI

La \_ commande de chargement MCI charge un fichier. Les appareils vidéo et vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Pointeur vers une structure de gestion de [**\_ \_ charge MCI**](mci-load-parms.md) . (Les appareils avec des paramètres supplémentaires peuvent remplacer cette structure par une structure spécifique à l’appareil. Pour les périphériques vidéo numériques, le paramètre **lpLoad** pointe vers une structure [**MCI \_ DGV \_ load \_ PARMS**](/previous-versions//dd743391(v=vs.85)) .)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

L’indicateur supplémentaire suivant s’applique à tous les appareils prenant en charge la \_ charge MCI :

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_charger le \_ fichier MCI
</dt> <dd>

Le membre **lpFileName** de la structure identifiée par *lpLoad* contient l’adresse d’une mémoire tampon contenant le nom de fichier.

</dd> </dl>

L’indicateur supplémentaire suivant est utilisé avec le type de périphérique de **superposition** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY MCI \_
</dt> <dd>

Le membre **RC** de la structure identifiée par *lpLoad* contient un rectangle d’affichage valide qui identifie la zone de la mémoire tampon vidéo à mettre à jour.

</dd> </dl>

Pour les périphériques de superposition vidéo, le paramètre *lpLoad* pointe vers une structure de paramètres de [**\_ \_ charge \_ MCI OVLY**](mci-ovly-load-parms.md) .

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

 


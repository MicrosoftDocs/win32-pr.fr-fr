---
title: Commande MCI_RESERVE (mmsystem. h)
description: La \_ commande de réserve MCI alloue de l’espace disque contigu à l’espace de travail de l’instance de pilote de périphérique afin de l’utiliser lors de l’enregistrement suivant. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- commande MCI_RESERVE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f21570d37fba9bc0c9595715715a9291aedd30650081edfa5d50f7264cf16c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803460"
---
# <a name="mci_reserve-command"></a>\_Commande de réserve MCI

La \_ commande de réserve MCI alloue de l’espace disque contigu à l’espace de travail de l’instance de pilote de périphérique afin de l’utiliser lors de l’enregistrement suivant. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
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

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ réserves \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Si l’espace de travail contient des données non enregistrées, ces données sont perdues. Si l’espace disque n’est pas réservé avant l’enregistrement, la commande [MCI \_ Record](mci-record.md) effectue une réservation implicite avec des paramètres par défaut spécifiques à l’appareil. Sur certaines implémentations, la réserve n’est pas obligatoire et peut être ignorée par le pilote de périphérique. La réservation explicite d’espace vous permet de mieux contrôler le moment où se produit l’allocation de disque, la quantité d’espace allouée et l’emplacement où l’espace disque est alloué. La quantité et l’emplacement de l’espace disque déjà réservé pour cette instance d’appareil peuvent être modifiés par l’émission d' \_ une nouvelle réserve MCI. Tout espace disque alloué et toujours inutilisé n’est pas libéré tant que les données enregistrées ne sont pas enregistrées ou que l’instance de pilote de périphérique n’est pas fermée.

Si la vidéo est désactivée avec l' \_ indicateur MCI désactivé de la commande [ \_ SETVIDEO MCI](mci-setvideo.md) , l’espace réservé n’inclut aucune vidéo. Si le son est désactivé avec l' \_ indicateur MCI désactivé de la [commande \_ SETAUDIO MCI](mci-setaudio.md) , l’espace réservé n’inclut aucun audio. Si les données audio et vidéo sont désactivées ou si la taille demandée est égale à zéro, aucun espace n’est réservé et tout espace réservé existant est libéré.

Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_réservation DGV \_ MCI \_ dans
</dt> <dd>

Le membre **lpstrPath** de la structure identifiée par *lpReserve* contient l’adresse d’une mémoire tampon contenant l’emplacement d’un fichier temporaire. La mémoire tampon contient uniquement le chemin d’accès du lecteur et du répertoire du fichier utilisé pour contenir les données enregistrées ; le nom de fichier est spécifié par le pilote de périphérique. Ce fichier temporaire est supprimé lorsque l’instance d’appareil est fermée, sauf si elle est enregistrée explicitement. Si cet indicateur est omis, le pilote de périphérique spécifie l’emplacement d’allocation de l’espace disque.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_taille de \_ réserve \_ DGV MCI
</dt> <dd>

Le membre **dwSize nul** de la structure identifiée par *lpReserve* spécifie la quantité approximative d’espace disque à réserver dans l’espace de travail pour l’enregistrement. La valeur est spécifiée dans le format d’heure actuel. La quantité d’espace disque est estimée à partir de l’heure demandée et à partir de laquelle le format de fichier et l’algorithme vidéo et audio et les valeurs de qualité sont en vigueur. Si cet indicateur est omis, le pilote de périphérique peut utiliser une valeur par défaut qu’il définit.

</dd> </dl>

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

 


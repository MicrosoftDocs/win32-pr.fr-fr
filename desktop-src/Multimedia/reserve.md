---
title: Reserve, commande
description: La commande Reserve alloue de l’espace disque contigu à l’espace de travail de l’instance de périphérique. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- commande reserve Windows multimédia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363916"
---
# <a name="reserve-command"></a>Reserve, commande

La commande Reserve alloue de l’espace disque contigu à l’espace de travail de l’instance de périphérique. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Un ou plusieurs des indicateurs suivants.



| Valeur           | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dans le *chemin*       | Spécifie le lecteur et le chemin d’accès au répertoire (mais pas le nom) d’un fichier temporaire utilisé pour contenir les données enregistrées. Le nom de ce fichier est spécifié par l’appareil. Le fichier temporaire est supprimé lorsque l’appareil est fermé. Si cet indicateur est omis, le périphérique spécifie l’emplacement de l’espace disque.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *durée* de la taille | Spécifie la quantité approximative d’espace disque à réserver dans l’espace de travail. La valeur de *durée* est spécifiée dans le format d’heure actuel. L’appareil base son estimation de l’espace disque requis sur les paramètres suivants : l’heure demandée, le format de fichier, l’algorithme de compression vidéo et audio et les valeurs de qualité de compression en vigueur. Si [setvideo](setvideo.md) « record » est « OFF », l’espace est réservé uniquement à l’audio. Si [SetAudio](setaudio.md) « record » est « OFF », l’espace est réservé uniquement pour la vidéo. Si les deux sont « OFF », ou si *Duration* est égal à zéro, aucun espace n’est réservé et tout espace réservé existant est libéré. Si cet indicateur est omis, l’appareil utilise une valeur par défaut définie par l’appareil. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Si nécessaire, les commandes [enregistrer ou](record.md) [Enregistrer](save.md) suivantes utilisent l’espace réservé par cette commande. Si l’espace de travail contient des données non enregistrées, les données sont perdues. Certains appareils ne nécessitent pas de réserve et l’ignorent. Si l’espace disque n’est pas réservé avant l’enregistrement, la commande d’enregistrement effectue une réservation implicite avec des indicateurs par défaut spécifiques à l’appareil. Utilisez une commande de réserve explicite si vous souhaitez mieux contrôler quand l’allocation de disque se produit, le contrôle de la quantité d’espace alloué et le contrôle de l’emplacement où l’espace disque est alloué. Votre application peut modifier la quantité et l’emplacement de l’espace disque précédemment réservé avec les commandes de réserve suivantes. Tout espace disque alloué et toujours inutilisé n’est pas libéré tant que les données enregistrées ne sont pas enregistrées ou que l’instance d’appareil n’est pas fermée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[enregistrement](record.md)
</dt> <dt>

[enregistrer](save.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 


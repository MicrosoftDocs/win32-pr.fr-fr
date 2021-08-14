---
title: commande Close (Corecrt \_ IO. h)
description: La commande fermer ferme l’appareil ou le fichier et toutes les ressources associées. MCI décharge un appareil lorsque toutes les instances de l’appareil ou tous les fichiers sont fermés. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- commande fermer Windows multimédia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807958"
---
# <a name="close-command"></a>commande Close

La commande fermer ferme l’appareil ou le fichier et toutes les ressources associées. MCI décharge un appareil lorsque toutes les instances de l’appareil ou tous les fichiers sont fermés. Tous les périphériques MCI reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Pour fermer tous les appareils ouverts par votre application, spécifiez l’identificateur de périphérique « tous » pour le paramètre *lpszDeviceID* .

La fermeture de l’appareil **cdaudio** arrête la lecture audio.

**Windows 2000/XP :** Si l’appareil **cdaudio** est en lecture, la fermeture de l’appareil **cdaudio** n’entraîne pas l’arrêt de la lecture de l’audio. Envoyez d’abord la commande [Stop](stop.md) .

## <a name="examples"></a>Exemples

La commande suivante ferme l’appareil « mySound ».

``` syntax
close mysound
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Corecrt \_ IO. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> </dl>

 


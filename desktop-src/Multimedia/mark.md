---
title: commande Mark
description: La commande Mark contrôle l’enregistrement et l’effacement des marques sur la bande vidéo. Les périphériques VCR reconnaissent cette commande.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- commande mark Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f59f56a6d542120d088d764d1b301329a7f0b167f25952587a9e743878643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138750"
---
# <a name="mark-command"></a>commande Mark

La commande Mark contrôle l’enregistrement et l’effacement des marques sur la bande vidéo. Les périphériques VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

Un des indicateurs suivants.



| Valeur | Signification                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Efface une marque à la position actuelle, s’il en existe une. Pour effacer une marque, commencez par Rechercher la marque, puis émettez la commande marquer l’effacement. |
| écrire | Écrit une marque à la position actuelle. Il se peut que le magnétoscope doive être en mode lecture ou enregistrement pour que cette commande aboutisse.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify » ou « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les marques sont des signaux spéciaux écrits dans le contenu qui peuvent être détectés par le magnétoscope lors de recherches à grande vitesse. Les marques sont spécifiques au magnétoscope.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> </dl>

 


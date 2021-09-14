---
title: copier (commande)
description: La commande de copie copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- commande de copie Windows multimédia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011803"
---
# <a name="copy-command"></a>copier (commande)

La commande de copie copie les données dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

L’un des indicateurs suivants identifiant l’élément à copier.



| Valeur                 | Signification                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*        | Spécifie la partie de chaque frame qui sera copiée. En cas d’omission, le paramètre par défaut est le cadre entier.                                                                                                                             |
| *flux* de flux audio | Spécifie le flux audio dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également copier la vidéo, vous devez également utiliser l’indicateur « flux vidéo ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont copiés.) |
| à partir de la *position*       | Spécifie le début de la plage copiée. En cas d’omission, le paramètre par défaut est la position actuelle.                                                                                                                                         |
| pour *positionner*         | Spécifie la fin de la plage copiée. Les données audio et vidéo copiées sont exclusives à cette position. En cas d’omission, le paramètre par défaut est la fin de l’espace de travail.                                                                       |
| *flux* de flux vidéo | Spécifie le flux vidéo dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également copier l’audio, vous devez également utiliser l’indicateur « flux audio ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont copiés.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

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

 


---
title: commande couper
description: La commande couper supprime les données de l’espace de travail et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- commande couper Windows multimédia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363731"
---
# <a name="cut-command"></a>commande couper

La commande couper supprime les données de l’espace de travail et les copie dans le presse-papiers. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
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

L’un des indicateurs suivants identifiant l’élément à couper.



| Valeur                 | Signification                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*        | Spécifie la partie de chaque coupe de cadre. En cas d’omission, la valeur par défaut est le frame entier. Lorsque cet élément est spécifié, les cadres ne sont pas supprimés. Au lieu de cela, la zone à l’intérieur du rectangle devient noire.                                       |
| *flux* de flux audio | Spécifie le flux audio dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également couper la vidéo, vous devez également utiliser l’indicateur « flux vidéo ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont coupés.) |
| à partir de la *position*       | Spécifie le début de la coupe de plage. En cas d’omission, sa valeur par défaut est la position actuelle.                                                                                                                                                |
| pour *positionner*         | Spécifie la fin de la coupe de plage. La coupure des données audio et vidéo est exclusive à cette position. S’il est omis, la valeur par défaut est la fin de l’espace de travail.                                                                                  |
| *flux* de flux vidéo | Spécifie le flux vidéo dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également couper le son, vous devez également utiliser l’indicateur « flux audio ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont coupés.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

La modification devient permanente uniquement lorsque les données sont enregistrées de manière explicite ; Toutefois, la lecture agit comme si les données avaient été supprimées.

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
</dt> </dl>

 


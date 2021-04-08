---
title: commande Delete
description: La commande Delete supprime un segment de données d’un fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- commande Delete Windows multimédia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844230"
---
# <a name="delete-command"></a>commande Delete

La commande Delete supprime un segment de données d’un fichier. Les périphériques vidéo numériques et Waveform-Audio reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

Indicateur qui identifie un segment de données à supprimer. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Delete** et les indicateurs utilisés par chaque type.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>au niveau du <em>rectangle</em></li>
<li><em>flux</em> de flux audio</li>
<li>à partir de la <em>position</em></li>
</ul></td>
<td><ul>
<li>pour <em>positionner</em></li>
<li><em>flux</em> de flux vidéo</li>
</ul></td>
</tr>
<tr class="even">
<td>WaveAudio</td>
<td>à partir de la <em>position</em></td>
<td>pour <em>positionner</em></td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre *lpszPosition* et leurs significations.



| Valeur                 | Signification                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*        | Spécifie la partie de chaque frame supprimée. En cas d’omission, la valeur par défaut est le frame entier. Lorsque cet élément est spécifié, les cadres ne sont pas supprimés. Au lieu de cela, la zone à l’intérieur du rectangle devient noire.                                          |
| *flux* de flux audio | Spécifie le flux audio dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également supprimer la vidéo, vous devez également utiliser l’indicateur « flux vidéo ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont supprimés.) |
| à partir de la *position*       | Spécifie la position de début de la suppression. Si cet indicateur est omis, la suppression commence à la position actuelle.                                                                                                                       |
| pour *positionner*         | Spécifie la position à laquelle la suppression se termine. Si cet indicateur est omis, la suppression se poursuit jusqu’à la fin du contenu ou de l’espace de travail.                                                                                                       |
| *flux* de flux vidéo | Spécifie le flux vidéo dans l’espace de travail affecté par la commande. Si vous utilisez cet indicateur et que vous souhaitez également supprimer l’audio, vous devez également utiliser l’indicateur « flux audio ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont supprimés.)     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Avant d’émettre des commandes qui utilisent des valeurs de position, vous devez définir le format d’heure souhaité à l’aide de la commande [Set](set.md) .

## <a name="examples"></a>Exemples

La commande suivante supprime les données Waveform-Audio de 1 milliseconde à 900 millisecondes (en supposant que le format d’heure est défini sur millisecondes).

``` syntax
delete mysound from 1 to 900
```

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
</dt> <dt>

[set](set.md)
</dt> </dl>

 


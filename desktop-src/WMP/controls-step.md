---
title: Controls. Step, méthode
description: La méthode STEP fait en sorte que l’élément multimédia vidéo actuel fige la lecture sur le frame suivant ou le frame précédent.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- méthode STEP du lecteur Windows Media
- Step, méthode lecteur Windows Media, classe Controls
- Classe Controls lecteur Windows Media, méthode STEP
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537475"
---
# <a name="controlsstep-method"></a>Controls. Step, méthode

La méthode **Step** fait en sorte que l’élément multimédia vidéo actuel fige la lecture sur le frame suivant ou le frame précédent.

## <a name="syntax"></a>Syntaxe


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*frameCount* \[ dans\]
</dt> <dd>

**Nombre** (**long**) indiquant le nombre de frames à exécuter avant le gel. Doit être défini à 1 ou-1.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ne prend actuellement en charge que les paramètres 1 ou-1. vous ne pouvez donc pas effectuer un pas à pas d’un seul Frame à la fois.

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> <dt>

[**Objet DVD**](dvd-object.md)
</dt> </dl>

 

 






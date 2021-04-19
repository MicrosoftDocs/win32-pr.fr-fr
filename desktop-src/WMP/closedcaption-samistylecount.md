---
title: ClosedCaption.SAMIStyleCount
description: La propriété SAMIStyleCount récupère le nombre de styles pris en charge par le fichier SAMI actuel.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Lecteur Windows Media ClosedCaption. SAMIStyleCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528624"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

La propriété **SAMIStyleCount** récupère le nombre de styles pris en charge par le fichier sami actuel.

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).

**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 






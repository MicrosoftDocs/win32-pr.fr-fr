---
title: ClosedCaption.SAMILangCount
description: La propriété SAMILangCount récupère le nombre de langues prises en charge par le fichier SAMI actuel.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Lecteur Windows Media ClosedCaption. SAMILangCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528693"
---
# <a name="closedcaptionsamilangcount"></a>ClosedCaption.SAMILangCount

La propriété **SAMILangCount** récupère le nombre de langues prises en charge par le fichier sami actuel.

``` syntax
player.closedCaption.SAMILangCount
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

[**ClosedCaption.getSAMILangName**](closedcaption-getsamilangname.md)
</dt> <dt>

[**ClosedCaption.SAMILang**](closedcaption-samilang.md)
</dt> </dl>

 

 






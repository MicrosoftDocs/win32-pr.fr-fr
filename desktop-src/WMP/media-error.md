---
title: Media. erreur
description: La propriété Error récupère un objet ErrorItem si l’élément multimédia a une condition d’erreur.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media. error Lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919152"
---
# <a name="mediaerror"></a>Media. erreur

La propriété **Error** récupère un objet **ErrorItem** si l’élément multimédia a une condition d’erreur.

## <a name="syntax"></a>Syntaxe

*lecteur*. *currentMedia*. **erreur**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet **ErrorItem** en lecture seule.

## <a name="remarks"></a>Notes

Si l’élément multimédia ne peut pas être lu, cette propriété récupère un objet **ErrorItem** qui contient des informations sur le problème rencontré.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> </dl>

 

 






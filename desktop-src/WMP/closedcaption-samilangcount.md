---
title: ClosedCaption.SAMILangCount
description: La propriété SAMILangCount récupère le nombre de langues prises en charge par le fichier SAMI actuel.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- ClosedCaption. SAMILangCount Lecteur Windows Media
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
ms.openlocfilehash: ecfcf9562639fe425915c9e0720cf7cf4cd75c5a56df66d8e6e2f31408145601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840308"
---
# <a name="closedcaptionsamilangcount"></a>ClosedCaption.SAMILangCount

La propriété **SAMILangCount** récupère le nombre de langues prises en charge par le fichier sami actuel.

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Remarques

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

 

 






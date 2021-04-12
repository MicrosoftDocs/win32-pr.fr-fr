---
description: Un descripteur HRECOWORDLIST est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance. Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Handle HRECOWORDLIST (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526572"
---
# <a name="hrecowordlist-handle"></a>Handle HRECOWORDLIST

Un descripteur **HRECOWORDLIST** est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance. Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Notes

La fonction suivante utilise un **HRECOWORDLIST**.



| Fonction                                         | Description                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Ajoute un ou plusieurs mots à la liste de mots.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Détruit la liste de mots active.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Crée une liste de mots.<br/>                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Récapitulatif</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SetWordList fonction)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 





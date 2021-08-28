---
description: Un descripteur HRECOWORDLIST est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance. Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Handle HRECOWORDLIST (Récapitulatifis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7384873f562627f54326cfca78883c9f3a02351dad1df0bf45a23b61b03c167d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967558"
---
# <a name="hrecowordlist-handle"></a>Handle HRECOWORDLIST

Un descripteur **HRECOWORDLIST** est utilisé pour gérer une liste de mots que vous attachez à un contexte de module de reconnaissance. Vous utilisez une liste de mots pour améliorer les résultats de la reconnaissance.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Remarques

La fonction suivante utilise un **HRECOWORDLIST**.



| Fonction                                         | Description                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Ajoute un ou plusieurs mots à la liste de mots.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Détruit la liste de mots active.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Crée une liste de mots.<br/>                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>Récapitulatif</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SetWordList fonction)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 





---
description: Représente une liste de mots qui peuvent être utilisés pour améliorer le résultat de la reconnaissance.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: InkWordList, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526273"
---
# <a name="inkwordlist-class"></a>InkWordList, classe

Représente une liste de mots qui peuvent être utilisés pour améliorer le résultat de la reconnaissance.

**InkWordList** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Méthodes](#methods)

### <a name="interfaces"></a>Interfaces

La classe **InkWordList** définit ces interfaces.



| Interface        | Description                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Cet objet implémente l’interface com **IInkWordList** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkWordList** possède ces méthodes.



| Méthode                                       | Description                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Ajoute un mot unique à **InkWordList**.<br/>                   |
| [**Fusion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Fusionne un autre **InkWordList** dans ce **InkWordList**.<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Supprime un mot unique d’un **InkWordList**.<br/>                |



 

## <a name="remarks"></a>Notes

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriété de la propriété de la propriété**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Constantes Factoid](factoid-constants.md)
</dt> <dt>

[**InkRecognizerContext, classe**](inkrecognizercontext-class.md)
</dt> </dl>

 


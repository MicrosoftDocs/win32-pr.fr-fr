---
description: Évalue une expression et affiche un message de diagnostic si l’expression a la valeur FALSe. Ignoré dans les builds de vente au détail.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: DÉCLARER la macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112193"
---
# <a name="assert-macro"></a>ASSERT (macro)

Évalue une expression et affiche un message de diagnostic si l’expression a la **valeur false**. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*185* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Dans les versions Debug, si l’expression est **false**, cette macro affiche une boîte de message avec le texte de l’expression, le nom du fichier source et le numéro de ligne. L’utilisateur peut ignorer l’assertion, entrer le débogueur ou quitter l’application.

## <a name="examples"></a>Exemples


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





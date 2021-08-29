---
description: Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne. L’utilisateur peut ignorer le message, entrer le débogueur ou quitter l’application. Ignoré dans les builds de vente au détail.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: DbgBreak macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: bb727a573efebc2957d5eaddfb32d077d981503fb7bd8a7c9481e6841dcd901a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052039"
---
# <a name="dbgbreak-macro"></a>DbgBreak macro)

Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne. L’utilisateur peut ignorer le message, entrer le débogueur ou quitter l’application. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strLiteral* 
</dt> <dd>

Chaîne de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="examples"></a>Exemples


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





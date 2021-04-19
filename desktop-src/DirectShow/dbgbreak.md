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
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527334"
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
| En-tête<br/> | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





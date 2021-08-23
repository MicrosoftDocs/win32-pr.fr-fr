---
description: La macro DbgLog envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés. Cette macro est ignorée dans les versions commerciales.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: DbgLog macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 619a3cd277425b555bc64139c3e59c959cc6abd19d6da22c2129830c38496a24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953338"
---
# <a name="dbglog-macro"></a>DbgLog macro)

La macro **DbgLog** envoie une chaîne à l’emplacement de sortie de débogage, si la journalisation est activée pour le type et le niveau spécifiés. Cette macro est ignorée dans les versions commerciales.

## <a name="syntax"></a>Syntaxe


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Types* 
</dt> <dd>

Combinaison d’opérations de bits d’un ou plusieurs types de messages.

</dd> <dt>

*Niveau* 
</dt> <dd>

Niveau de journalisation pour ce message.

</dd> <dt>

*pFormat* 
</dt> <dd>

Chaîne de format **printf** -style.

</dd> <dt>

*...* 
</dt> <dd>

Arguments supplémentaires pour la chaîne de format.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si la journalisation du débogage de l’un des types de messages est définie au niveau spécifié ou supérieur, cette macro envoie la chaîne mise en forme à l’emplacement de sortie de débogage.

La macro ajoute automatiquement un caractère de saut de ligne à la chaîne de sortie.

> [!Note]  
> Un ensemble supplémentaire de parenthèses doit contenir les paramètres de macro :

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 





---
description: Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.
title: MRUCMPPROC, fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: bcf8bb7c8ec4ceab299efd75c61cabe86f43d0ee46585be59ab4000957554ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111489"
---
# <a name="mrucmpproc-callback-function"></a>MRUCMPPROC, fonction de rappel

Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.

## <a name="syntax"></a>Syntaxe


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pString1* 
</dt> <dd>

Type : **LPCTSTR**

Première chaîne.

</dd> <dt>

*pString2* 
</dt> <dd>

Type : **LPCTSTR**

Deuxième chaîne à comparer au premier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Retourne 0 si les éléments sont identiques, une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette fonction peut éventuellement être spécifiée pour être utilisée dans la structure [**MRUINFO**](mruinfo.md) transmise à [**CreateMRUListW**](createmrulist.md). Cela est utile lorsque la liste MRU a été créée avec l’indicateur **\_ binaire MRU** . Lorsque cette fonction n’est pas spécifiée, les fonctions de comparaison de chaînes standard sont utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>            |
| Noms Unicode et ANSI<br/>   | **MRUCMPPROCW** (Unicode) et **MRUCMPPROCA** (ANSI)<br/> |



 

 





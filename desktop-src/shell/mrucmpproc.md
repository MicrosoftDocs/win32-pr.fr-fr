---
description: Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.
title: MRUCMPPROC fonction de rappel
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
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840780"
---
# <a name="mrucmpproc-callback-function"></a>MRUCMPPROC fonction de rappel

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

## <a name="return-value"></a>Valeur renvoyée

Type : **int**

Retourne 0 si les éléments sont identiques, une valeur différente de zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Cette fonction peut éventuellement être spécifiée pour être utilisée dans la structure [**MRUINFO**](mruinfo.md) transmise à [**CreateMRUListW**](createmrulist.md). Cela est utile lorsque la liste MRU a été créée avec l’indicateur **\_ binaire MRU** . Lorsque cette fonction n’est pas spécifiée, les fonctions de comparaison de chaînes standard sont utilisées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>            |
| Noms Unicode et ANSI<br/>   | **MRUCMPPROCW** (Unicode) et **MRUCMPPROCA** (ANSI)<br/> |



 

 





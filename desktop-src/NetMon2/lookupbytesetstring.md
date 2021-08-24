---
description: La fonction LookupByteSetString retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: LookupByteSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 208f7cef1a658ae321d7ce03aaee763e5387b5a45985d59134418a4d136e0b56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742499"
---
# <a name="lookupbytesetstring-function"></a>LookupByteSetString fonction)

La fonction **LookupByteSetString** retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpSet* 
</dt> <dd>

Pointeur vers un jeu étiqueté, à partir duquel vous pouvez extraire l’étiquette de la valeur.

</dd> <dt>

*Valeur* 
</dt> <dd>

Valeur d’un jeu étiqueté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une chaîne qui correspond à la valeur fournie.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





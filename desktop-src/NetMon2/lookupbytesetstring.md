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
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194687"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est une chaîne qui correspond à la valeur fournie.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





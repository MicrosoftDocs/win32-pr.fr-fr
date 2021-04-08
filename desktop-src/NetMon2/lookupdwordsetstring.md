---
description: La fonction LookupDwordSetString retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: LookupDwordSetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752188"
---
# <a name="lookupdwordsetstring-function"></a>LookupDwordSetString fonction)

La fonction **LookupDwordSetString** retourne la chaîne correspondant à la valeur spécifiée d’un jeu étiqueté.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpSet* 
</dt> <dd>

Ensemble étiqueté, à partir duquel vous pouvez extraire l’étiquette de la valeur.

</dd> <dt>

*Valeur* 
</dt> <dd>

Valeur d’un jeu étiqueté.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est la chaîne qui correspond à la valeur spécifiée.

Si la fonction échoue, la valeur spécifiée n’est pas dans l’ensemble, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 





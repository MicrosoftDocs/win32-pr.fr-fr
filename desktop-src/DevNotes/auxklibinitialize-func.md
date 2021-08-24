---
description: Initialise la \_ bibliothèque klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Fonction AuxKlibInitialize (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654879"
---
# <a name="auxklibinitialize-function"></a>AuxKlibInitialize fonction)

Initialise la \_ bibliothèque klib. Cette fonction doit être appelée avant que toute autre fonction de la bibliothèque puisse être appelée.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est STATUs \_ successful.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’État définis dans Ntstatus. h, qui est disponible dans le kit WDK.

## <a name="remarks"></a>Remarques

La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|------------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque d’API auxiliaire version 1,0 ou ultérieure<br/>                            |
| En-tête<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl>   |
| Bibliothèque<br/>         | <dl> <dt>Aux \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 





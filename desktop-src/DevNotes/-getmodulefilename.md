---
description: Obtient le chemin d’accès du module.
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542722"
---
# <a name="_getmodulefilename-function"></a>\_GetModuleFileName, fonction

\[Cette fonction est un wrapper sur la fonction **GetModuleFileName** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **GetModuleFileName** directement.\]

Obtient le chemin d’accès du module. Consultez [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).

## <a name="syntax"></a>Syntaxe


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 

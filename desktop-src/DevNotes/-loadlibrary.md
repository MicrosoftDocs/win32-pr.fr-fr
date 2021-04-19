---
description: Charge une bibliothèque.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542484"
---
# <a name="_loadlibrary-function"></a>\_Fonction LoadLibrary

\[Cette fonction est un wrapper sur la fonction **LoadLibrary** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **LoadLibrary** directement.\]

Charge une bibliothèque. Consultez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).

## <a name="syntax"></a>Syntaxe


```C++
HMODULE _LoadLibrary(
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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 

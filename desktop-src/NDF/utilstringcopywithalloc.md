---
title: UtilStringCopyWithAlloc, fonction (Ndattributils. h)
description: Alloue et copie une chaîne source.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011627"
---
# <a name="utilstringcopywithalloc-function"></a>UtilStringCopyWithAlloc fonction)

La fonction **UtilStringCopyWithAlloc** alloue et copie une chaîne source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Type : **LPWStr \***

Emplacement de stockage du pointeur vers la mémoire allouée. Quand vous n’en avez plus besoin, il doit être libéré avec [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree). Cette mémoire tampon se termine toujours par un caractère null.

</dd> <dt>

*BufferMax* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre maximal de caractères à lire à partir de la *source*.

</dd> <dt>

*Source* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Chaîne à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                  | Description                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération a réussi.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 


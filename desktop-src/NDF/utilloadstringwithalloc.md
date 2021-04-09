---
title: UtilLoadStringWithAlloc, fonction (Ndattributils. h)
description: Alloue et charge une chaîne à partir de la table de ressources.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106501"
---
# <a name="utilloadstringwithalloc-function"></a>UtilLoadStringWithAlloc fonction)

La fonction **UtilLoadStringWithAlloc** alloue et charge une chaîne à partir de la table de ressources.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uID* \[ dans\]
</dt> <dd>

Type : **uint**

Identificateur de de la chaîne à charger.

</dd> <dt>

*ppwzBuffer* \[ à\]
</dt> <dd>

Tapez : **LPWStr \** _

Emplacement où la chaîne qui vient d’être allouée sera placée. La chaîne doit être libérée à l’aide de [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) lorsqu’elle n’est plus nécessaire.

</dd> <dt>

*cchBufferMax* \[ dans\]
</dt> <dd>

Type : **uint**

Nombre maximal de caractères à charger à partir de la table de ressources. Si la chaîne de ressource dépasse le nombre de caractères spécifié, elle est tronquée et se termine par null.

> [!Note]  
> Ce paramètre ne peut pas être défini à zéro.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                  | Description                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération a réussi.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


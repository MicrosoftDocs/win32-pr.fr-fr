---
description: Définit le filtre de correspondance du modèle d’objet BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: SetNPPPatternFilterInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194564"
---
# <a name="setnpppatternfilterinblob-function"></a>SetNPPPatternFilterInBlob fonction)

La fonction **SetNPPPatternFilterInBlob** définit le filtre de correspondance du modèle d’objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*pExpression* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [expression](expression.md) qui définit l’expression de filtre définie.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle d’un objet BLOB d’erreurs qui spécifie à quel endroit de l’objet BLOB d’origine l’erreur (le cas échéant) s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction **SetNPPPatternFilterInBlob** réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="remarks"></a>Notes

Les correspondances de modèle filtrent les données stockées dans la catégorie de **configuration** de l’objet BLOB.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 





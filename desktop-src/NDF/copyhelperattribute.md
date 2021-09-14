---
title: CopyHelperAttribute, fonction (Ndattributils. h)
description: Crée une copie d’une structure d' \_ attribut d’assistance.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute fonction NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110510"
---
# <a name="copyhelperattribute-function"></a>CopyHelperAttribute fonction)

La fonction **CopyHelperAttribute** crée une copie d’une structure d' [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dest* \[ . à\]
</dt> <dd>

Type : **[ **\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Structure à mettre à jour.

</dd> <dt>

*Source* \[ dans\]
</dt> <dd>

Type : **\* [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) const**

Structure existante à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                   | Description                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération a réussi.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour terminer cette opération.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**attribut d’assistance \_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 






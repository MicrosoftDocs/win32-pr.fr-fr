---
title: CopyRootCauseInfo, fonction (Ndattributils. h)
description: Crée une copie d’une structure RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo fonction NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941910"
---
# <a name="copyrootcauseinfo-function"></a>CopyRootCauseInfo fonction)

La fonction **CopyRootCauseInfo** crée une copie d’une structure [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dest* \[ . à\]
</dt> <dd>

Tapez : **[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Structure à mettre à jour.

</dd> <dt>

_Source * \[ dans\]
</dt> <dd>

Type : **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Structure existante à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.



| Code de retour                                                                                   | Description                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération a réussi.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs paramètres n’ont pas été fournis correctement.<br/>          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour terminer cette opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 






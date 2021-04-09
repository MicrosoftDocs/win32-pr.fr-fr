---
title: FreeRootCauseInfos, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos fonction NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740893"
---
# <a name="freerootcauseinfos-function"></a>FreeRootCauseInfos fonction)

La fonction **FreeRootCauseInfos** libère la mémoire allouée en interne à un tableau de structures [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) . Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Tapez : **[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Tableau de structures. La mémoire allouée pointée par ces structures sera libérée.

</dd> <dt>

_RootCauseCount * 
</dt> <dd>

Type : **ULong**

Nombre de structures dans le tableau pointé par *pinfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Type : **bool**

True si le tableau de structures doit également être supprimé ; Sinon, false.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


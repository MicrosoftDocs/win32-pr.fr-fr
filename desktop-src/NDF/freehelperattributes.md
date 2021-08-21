---
title: FreeHelperAttributes, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures d' \_ attributs d’assistance.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- FreeHelperAttributes fonction NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb16ad2d7f505a90d806e3f6a155f2c20affce2c71267316c2278e2320c371b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802429"
---
# <a name="freehelperattributes-function"></a>FreeHelperAttributes fonction)

La fonction **FreeHelperAttributes** libère la mémoire allouée en interne à un tableau de structures d' [**\_ attributs d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Type : **[ **\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Tableau de structures. La mémoire allouée pointée par ces structures sera libérée.

</dd> <dt>

*HelperAttributeCount* 
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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**attribut d’assistance \_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


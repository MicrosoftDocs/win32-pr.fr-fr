---
title: FreeSoHAttributeValue, fonction (NapUtil. h)
description: Libère une structure de données SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue fonction NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413825"
---
# <a name="freesohattributevalue-function"></a>FreeSoHAttributeValue fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **FreeSoHAttributeValue** libère une structure de données [**SoHAttributeValue**](sohattributevalue-union.md) .

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Valeur [**SoHAttributeType**](sohattributetype-enum.md) qui spécifie le type de valeur d’attribut SoH à libérer.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Pointeur vers le [**SoHAttributeValue**](sohattributevalue-union.md) à libérer.

</dd> </dl>

## <a name="remarks"></a>Notes

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :

-   Les paramètres **in** sont alloués et libérés par l’appelant.
-   Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.
-   Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.

Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 






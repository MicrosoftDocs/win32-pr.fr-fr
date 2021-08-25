---
title: AllocFixupInfo, fonction (NapUtil. h)
description: Alloue de la mémoire pour une structure FixupInfo de la taille spécifiée.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- AllocFixupInfo fonction NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95ce329a433439716700b6ffc990d446c5d22faab91fa256f6abc0c73734327d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803489"
---
# <a name="allocfixupinfo-function"></a>AllocFixupInfo fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **AllocFixupInfo** alloue de la mémoire pour une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) de la taille spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fixupInfo* \[ in, out\]
</dt> <dd>

Pointeur vers l’adresse d’une structure [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) qui vient d’être allouée.

</dd> <dt>

*countResultCodes* \[ dans\]
</dt> <dd>

Nombre de codes de résultats à allouer à *fixupInfo*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                   | Description                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un argument non valide a été passé.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire virtuelle du système est insuffisante. Cette opération a échoué.<br/> |



 

## <a name="remarks"></a>Remarques

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :

-   Les paramètres **in** sont alloués et libérés par l’appelant.
-   Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.
-   Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.

Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 






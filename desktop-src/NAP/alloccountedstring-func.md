---
title: AllocCountedString, fonction (NapUtil. h)
description: Alloue de la mémoire pour une chaîne terminée par le caractère null et la retourne dans une structure CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString fonction NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510519"
---
# <a name="alloccountedstring-function"></a>AllocCountedString fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **AllocCountedString** alloue de la mémoire pour une chaîne terminée par le caractère null et la retourne dans une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*countedString* \[ in, out\]
</dt> <dd>

Pointeur vers l’adresse d’une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui vient d’être allouée.

</dd> <dt>

*chaîne* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui doit être retournée dans *countedString*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                   | Description                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un argument non valide a été passé.<br/>                                 |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire virtuelle du système est insuffisante. Cette opération a échoué.<br/> |



 

## <a name="remarks"></a>Notes

Toutes les interfaces COM prises en charge par le système NAP utilisent des règles de gestion de mémoire COM standard et les allocateurs de mémoire COM (**CoTaskMemAlloc** et **CoTaskMemFree**) :

-   Les paramètres **in** sont alloués et libérés par l’appelant.
-   Les paramètres **out** sont alloués par l’appelé et libérés par l’appelant à l’aide de **CoTaskMem**.
-   Les paramètres **in/out** sont alloués par l’appelant, libérés et réalloués par l’appelé, et libérés au final par l’appelant, à l’aide de **CoTaskMem**.

Toutes les fonctions NAP pour libérer de la mémoire libèrent également tous les pointeurs incorporés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 






---
description: La fonction ExpertMemorySize retourne la quantité de mémoire allouée par la fonction ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: ExpertMemorySize, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744269"
---
# <a name="expertmemorysize-function"></a>ExpertMemorySize fonction)

La fonction **ExpertMemorySize** retourne la quantité de mémoire allouée par la fonction [ExpertAllocMemory](expertallocmemory.md) .

## <a name="syntax"></a>Syntaxe


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*pOriginalMemory* \[ dans\]
</dt> <dd>

Pointeur vers l’adresse mémoire de l’expert alloué par [ExpertAllocMemory](expertallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la quantité de mémoire allouée en octets.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur le type de données **size \_ T** renvoyé par **ExpertMemorySize** , consultez types de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





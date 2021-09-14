---
description: La fonction ExpertFreeMemory libère de la mémoire acquise par les appels aux fonctions ExpertAllocMemory et ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: ExpertFreeMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021110"
---
# <a name="expertfreememory-function"></a>ExpertFreeMemory fonction)

La fonction **ExpertFreeMemory** libère de la mémoire acquise par les appels aux fonctions [**ExpertAllocMemory**](expertallocmemory.md) et [**ExpertReallocMemory**](expertreallocmemory.md) .

## <a name="syntax"></a>Syntaxe


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*pMemory* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire que Moniteur réseau alloue. Le pointeur *pMemory* peut être retourné par un appel précédent à [**ExpertAllocMemory**](expertallocmemory.md) ou [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit. la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour indique la raison de l’échec. Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert nettoie immédiatement et retourne.

## <a name="remarks"></a>Notes

Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau pour la gestion de la mémoire. Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





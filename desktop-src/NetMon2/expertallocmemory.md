---
description: La fonction ExpertAllocMemory alloue de la mémoire à l’expert.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: ExpertAllocMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd932a5330baf687d5578bac4e4bfac77ad4f5bad0560263ab7f1e8832e61fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890849"
---
# <a name="expertallocmemory-function"></a>ExpertAllocMemory fonction)

La fonction **ExpertAllocMemory** alloue de la mémoire à l’expert.

## <a name="syntax"></a>Syntaxe


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*nBytes* \[ dans\]
</dt> <dd>

Mémoire allouée, mesurée en octets.

</dd> <dt>

*perror* \[ à\]
</dt> <dd>

Indicateur d’erreur. Si la fonction échoue, le paramètre *nBytes* contient le code d’erreur. Si le code d’erreur est NMERR \_ expert \_ Terminate, l’expert doit le nettoyer et le renvoyer immédiatement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée.

Si la fonction échoue, la valeur de retour est **null** et *perror* fournit un code d’erreur qui indique la raison de l’échec.

## <a name="remarks"></a>Remarques

Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau (y compris [ExpertReallocMemory](expertreallocmemory.md)) pour la gestion de la mémoire. Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





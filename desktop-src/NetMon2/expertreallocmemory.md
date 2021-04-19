---
description: La fonction ExpertReallocMemory augmente ou diminue la quantité de mémoire allouée par Moniteur réseau.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: ExpertReallocMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514786"
---
# <a name="expertreallocmemory-function"></a>ExpertReallocMemory fonction)

La fonction **ExpertReallocMemory** augmente ou diminue la quantité de mémoire allouée par Moniteur réseau.

## <a name="syntax"></a>Syntaxe


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur unique transmis à l’expert lors de l' [**exécution**](run.md) ou de la [**configuration**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire allouée par Moniteur réseau. Le pointeur *pOriginalMemory* peut être retourné par un appel précédent à [**ExpertAllocMemory**](expertallocmemory.md) ou **ExpertReallocMemory**.

</dd> <dt>

*nBytes* \[ dans\]
</dt> <dd>

Taille de la mémoire réallouée.

</dd> <dt>

*perror* \[ à\]
</dt> <dd>

Au retour, code d’erreur si la fonction échoue. Si le code d’erreur est NMERR \_ expert \_ Terminate, l’expert doit le nettoyer et le retourner immédiatement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée.

Si la fonction échoue, la valeur de retour est **null** et *perror* (s’il s’agit d’une valeur non **null** ) indique la raison de l’échec.

## <a name="remarks"></a>Notes

Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau pour la gestion de la mémoire. Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





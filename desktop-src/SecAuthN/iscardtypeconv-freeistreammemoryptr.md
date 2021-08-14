---
description: Libère le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par une interface COM IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'ISCardTypeConv :: FreeIStreamMemoryPtr, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 62e91f9d8fca06c812370091b407edb73fed433a4c576857a7e089db28d6d856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922388"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>ISCardTypeConv :: FreeIStreamMemoryPtr, méthode

\[La méthode **FreeIStreamMemoryPtr** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **FreeIStreamMemoryPtr** libère le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par une interface com **IStream** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStrm* \[ dans\]
</dt> <dd>

Pointeur vers l’interface **IStream** qui gère le bloc de mémoire pointé par *pMem*.

</dd> <dt>

*PMEM* \[ dans\]
</dt> <dd>

Pointeur vers le bloc de mémoire géré par l’interface **IStream** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Mémoire allouée avec succès.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un paramètre de type pointeur était incorrect.<br/>                                            |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire libre insuffisante pour satisfaire la demande.<br/>                                            |



 

## <a name="remarks"></a>Remarques

Cette fonction libère complètement et correctement le pointeur d’octet pointant vers le bloc de mémoire HGLOBAL géré par l’interface **IStream** . Le pointeur d’octet est acquis par un appel à [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valeurs de retour de carte à puce](authentication-return-values.md)
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 

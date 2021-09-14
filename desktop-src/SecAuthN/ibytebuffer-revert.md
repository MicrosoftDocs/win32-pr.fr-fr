---
description: 'La méthode Revert ignore toutes les modifications apportées à un flux transactionnel depuis le dernier appel de IByteBuffer :: Commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'IByteBuffer :: Revert, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011300"
---
# <a name="ibytebufferrevert-method"></a>IByteBuffer :: Revert, méthode

\[La méthode **Revert** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Revert** ignore toutes les modifications apportées à un flux transactionnel depuis le dernier appel de [**IByteBuffer :: Commit**](ibytebuffer-commit.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi et que le flux a été rétabli à sa version précédente.

## <a name="remarks"></a>Notes

Cette méthode ignore les modifications apportées à un flux transactionnel depuis la dernière opération de validation.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la restauration d’un flux transactionnel avec la dernière opération validée.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 


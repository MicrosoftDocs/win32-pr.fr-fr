---
description: La méthode Commit garantit que toutes les modifications apportées à un objet ouvert en mode transactionnel sont reflétées dans le stockage parent.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer :: Commit, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: af165e6f0a805532eade820dcb67968a77186cee3f90cfc48a240d387b1f31b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127409"
---
# <a name="ibytebuffercommit-method"></a>IByteBuffer :: Commit, méthode

\[La méthode de **validation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Commit** garantit que toutes les modifications apportées à un objet ouvert en mode transactionnel sont reflétées dans le stockage parent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*grfCommitFlags* \[ dans\]
</dt> <dd>

Contrôle comment les modifications apportées à un objet de flux sont validées. Pour obtenir une définition de ces valeurs, consultez l’énumération STGC.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

Cette méthode garantit que les modifications apportées à un objet de flux ouvert en mode traité sont reflétées dans le stockage parent. Les modifications apportées au flux depuis son ouverture ou la dernière validation sont reflétées dans l’objet de stockage parent. Si le parent est ouvert en mode traité, le parent peut toujours revenir ultérieurement à la restauration des modifications apportées à cet objet de flux. L’implémentation de fichier composé ne prend pas en charge l’ouverture de flux en mode traité. cette méthode a donc très peu d’effet que de vider les mémoires tampons.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la validation des modifications apportées au stockage.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a>Configuration requise



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



 


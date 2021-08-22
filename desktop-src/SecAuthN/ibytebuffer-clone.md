---
description: La méthode Clone crée un nouvel objet avec son propre pointeur de recherche qui référence les mêmes octets que l’objet IByteBuffer d’origine.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer :: Clone, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fae7fbe32b18a81557200b5c5519092bb2edd84290d9909cf884308a9173aac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417679"
---
# <a name="ibytebufferclone-method"></a>IByteBuffer :: Clone, méthode

\[La méthode **clone** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **clone** crée un nouvel objet avec son propre pointeur de recherche qui référence les mêmes octets que l’objet [**IByteBuffer**](ibytebuffer.md) d’origine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppByteBuffer* \[ à\]
</dt> <dd>

En cas de réussite, pointe vers l’emplacement d’un pointeur [**IByteBuffer**](ibytebuffer.md) vers le nouvel objet de flux. Lorsque vous avez terminé d’utiliser le pointeur **IByteBuffer** , libérez-le en appelant la fonction [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Si une erreur se produit, ce paramètre a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

Cette méthode crée un nouvel objet de flux pour accéder aux mêmes octets, mais à l’aide d’un pointeur de recherche distinct. Le nouvel objet de flux voit les mêmes données que l’objet de flux source. Les modifications écrites dans un objet sont immédiatement visibles dans l’autre. Le verrouillage de plage est partagé entre les objets de flux.

Le paramètre initial du pointeur de recherche dans l’instance de flux cloné est le même que le paramètre actuel du pointeur de recherche dans le flux d’origine au moment de l’opération de clonage.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le clonage de l’interface [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
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



 


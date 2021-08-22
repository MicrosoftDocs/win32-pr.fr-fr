---
description: La méthode Initialize prépare l’objet IByteBuffer en vue de son utilisation. Cette méthode doit être appelée avant d’appeler d’autres méthodes dans l’interface IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'IByteBuffer :: Initialize, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417629"
---
# <a name="ibytebufferinitialize-method"></a>IByteBuffer :: Initialize, méthode

\[La méthode **Initialize** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Initialize** prépare l’objet [**IByteBuffer**](ibytebuffer.md) en vue de son utilisation. Cette méthode doit être appelée avant d’appeler d’autres méthodes dans l’interface **IByteBuffer** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lSize* \[ dans\]
</dt> <dd>

Taille initiale, en octets, des données que le flux doit contenir.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Si la **valeur** n’est pas null, il s’agit des données initiales à écrire dans le flux.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

Quand vous utilisez un nouveau flux [**IByteBuffer**](ibytebuffer.md) , appelez cette méthode avant d’utiliser l’une des autres méthodes **IByteBuffer** .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’initialisation de l’objet [**IByteBuffer**](ibytebuffer.md) .


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
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



 


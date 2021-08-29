---
description: Obtient un IMemoryBuffer sous la forme d’un tableau d’octets.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'IMemoryBufferByteAccess :: GetBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: df4e7897999dabd3ef7faff7d1e6f6b73c66f721256630e3ef91b154f4833b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758669"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a>IMemoryBufferByteAccess :: GetBuffer, méthode

Obtient un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) sous la forme d’un tableau d’octets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’octets contenant les données de la mémoire tampon.

</dd> <dt>

*capacité* \[ à\]
</dt> <dd>

Nombre d’octets dans le tableau retourné

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Quand [**MemoryBuffer :: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) est appelé, le code qui utilise cette mémoire tampon doit définir le pointeur de *valeur* sur null.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))
</dt> </dl>

 

 

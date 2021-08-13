---
description: La méthode CopyTo copie un nombre spécifié d’octets à partir du pointeur de recherche actuel dans l’objet vers le pointeur de recherche actuel dans un autre objet.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'IByteBuffer :: CopyTo, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4c4dc3861120d56dd5bff13fe1e77fd97e1fc32efed9622f18ee51b5160d1c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417639"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer :: CopyTo, méthode

\[La méthode **CopyTo** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **CopyTo** copie un nombre spécifié d’octets à partir du pointeur de recherche actuel dans l’objet vers le pointeur de recherche actuel dans un autre objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pByteBuffer* \[ dans\]
</dt> <dd>

Pointe vers le flux de destination. Le flux vers lequel pointe *pByteBuffer* peut être un nouveau flux ou un clone du flux source.

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Nombre d’octets à copier à partir du flux source.

</dd> <dt>

*pcbRead* \[ à\]
</dt> <dd>

Pointeur vers l’emplacement où cette méthode écrit le nombre réel d’octets lus à partir de la source. Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur. Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets lus.

</dd> <dt>

*pcbWritten* \[ à\]
</dt> <dd>

Pointeur vers l’emplacement où cette méthode écrit le nombre réel d’octets écrits dans la destination. Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur. Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets écrits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

Cette méthode copie les octets spécifiés d’un flux vers un autre. Elle peut également être utilisée pour copier un flux vers lui-même. Le pointeur de recherche dans chaque instance de flux est ajusté pour le nombre d’octets lus ou écrits.

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



 


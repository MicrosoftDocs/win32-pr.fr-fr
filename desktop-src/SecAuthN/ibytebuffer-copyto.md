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
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210027"
---
# <a name="ibytebuffercopyto-method"></a>IByteBuffer :: CopyTo, méthode

\[La méthode **CopyTo** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

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

## <a name="remarks"></a>Notes

Cette méthode copie les octets spécifiés d’un flux vers un autre. Elle peut également être utilisée pour copier un flux vers lui-même. Le pointeur de recherche dans chaque instance de flux est ajusté pour le nombre d’octets lus ou écrits.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 


---
description: 'Supprime les restrictions d’accès sur une plage d’octets précédemment restreinte à l’aide de IByteBuffer :: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'IByteBuffer :: UnlockRegion, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096409"
---
# <a name="ibytebufferunlockregion-method"></a>IByteBuffer :: UnlockRegion, méthode

\[La méthode **UnlockRegion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **UnlockRegion** supprime la restriction d’accès sur une plage d’octets précédemment restreinte à l’aide de [**IByteBuffer :: LockRegion**](ibytebuffer-lockregion.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Liboffset* \[ dans\]
</dt> <dd>

Offset d’octet pour le début de la plage.

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Longueur, en octets, de la plage à limiter.

</dd> <dt>

*dwLockType* \[ dans\]
</dt> <dd>

Restrictions d’accès précédemment placées dans la plage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Notes

La méthode **IByteBuffer :: UnlockRegion** déverrouille une région précédemment verrouillée à l’aide de la méthode [**IByteBuffer :: LockRegion**](ibytebuffer-lockregion.md) . Les régions verrouillées doivent être déverrouillées par la suite en appelant **IByteBuffer :: UnlockRegion** avec exactement les mêmes valeurs pour les paramètres *liboffset*, *CB* et *dwLockType* . La région doit être déverrouillée avant la libération du flux. Deux régions adjacentes ne peuvent pas être verrouillées séparément, puis déverrouillées à l’aide d’un seul appel de déverrouillage.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le déverrouillage d’une plage d’octets.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
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



 


---
description: Restreint l’accès à une plage d’octets spécifiée dans l’objet de mémoire tampon.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer :: LockRegion, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210024"
---
# <a name="ibytebufferlockregion-method"></a>IByteBuffer :: LockRegion, méthode

\[La méthode **LockRegion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **LockRegion** restreint l’accès à une plage d’octets spécifiée dans l’objet buffer.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Liboffset* \[ dans\]
</dt> <dd>

Entier qui spécifie l’offset d’octet pour le début de la plage.

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Entier qui spécifie la longueur de la plage, en octets, à limiter.

</dd> <dt>

*dwLockType* \[ dans\]
</dt> <dd>

Spécifie les restrictions requises pour accéder à la plage. Il peut s’agir de l’une des valeurs du tableau suivant.



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**écriture de verrou \_**</dt> </dl>             | La plage d’octets spécifiée peut être ouverte et lue un nombre quelconque de fois, mais l’écriture dans la plage verrouillée est interdite, à l’exception du propriétaire qui a obtenu ce verrou.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**VERROU \_ exclusif**</dt> </dl> | L’écriture dans la plage d’octets spécifiée est interdite, à l’exception du propriétaire auquel ce verrou a été accordé.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**VERROUILLER \_ ONLYONCE**</dt> </dl>    | Si ce verrou est accordé, aucun autre verrou \_ ONLYONCE de verrou ne peut être obtenu sur la plage. En général, ce type de verrou est un alias pour un autre type de verrou. Ainsi, les implémentations spécifiques peuvent avoir un comportement supplémentaire associé à ce type de verrou.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Notes

La plage d’octets peut s’étendre au-delà de la fin actuelle du flux. Le verrouillage au-delà de la fin d’un flux est utile comme méthode de communication entre les différentes instances du flux sans modifier les données qui font réellement partie du flux.

Trois types de verrouillage peuvent être pris en charge : le verrouillage pour exclure d’autres enregistreurs, le verrouillage pour exclure d’autres lecteurs ou Writers et le verrouillage qui permet à un seul demandeur d’obtenir un verrou sur la plage donnée, qui est généralement un alias pour l’un des deux autres types de verrous. Une instance de flux donnée peut prendre en charge l’un des deux premiers types, ou les deux. Le type de verrou est spécifié par *dwLockType*, à l’aide d’une valeur issue de l’énumération [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .

Toute région verrouillée avec la fonction **LockRegion** doit ensuite être déverrouillée explicitement en appelant [**IByteBuffer :: UnlockRegion**](ibytebuffer-unlockregion.md) avec exactement les mêmes valeurs pour les paramètres *liboffset*, *CB* et *dwLockType* . La région doit être déverrouillée avant la libération du flux. Deux régions adjacentes ne peuvent pas être verrouillées séparément, puis déverrouillées à l’aide d’un seul appel de déverrouillage.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la restriction de l’accès à une plage d’octets.


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



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



 


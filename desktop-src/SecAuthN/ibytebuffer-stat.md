---
description: La méthode stat récupère les informations statistiques de l’objet de flux.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'IByteBuffer :: stat, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dd80b408765985b2e009b2e580eb1bf81b08cb5ea1f2e7aaa5ed628a76073a27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127399"
---
# <a name="ibytebufferstat-method"></a>IByteBuffer :: stat, méthode

\[La méthode **Stat** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Stat** récupère les informations statistiques de l’objet de flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pstatstg* \[ à\]
</dt> <dd>

Pointe vers une structure **STATSTRUCT** où cette méthode place des informations sur cet objet de flux. Ce pointeur est **null** si une erreur se produit.

</dd> <dt>

*grfStatFlag* \[ dans\]
</dt> <dd>

Spécifie que cette méthode ne retourne pas certains des champs de la structure **STATSTRUCT** , ce qui entraîne l’enregistrement d’une opération d’allocation de mémoire. Les valeurs sont extraites de l’énumération [**StatFlag**](/windows/win32/api/wtypes/ne-wtypes-statflag)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

La méthode **IByteBuffer :: stat** récupère un pointeur vers la structure **STATSTRUCT** qui contient des informations sur ce flux ouvert.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer des informations statistiques à partir du flux.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
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



 


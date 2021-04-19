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
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521141"
---
# <a name="ibytebufferstat-method"></a>IByteBuffer :: stat, méthode

\[La méthode **Stat** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 


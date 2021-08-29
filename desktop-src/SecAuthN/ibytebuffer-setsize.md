---
description: La méthode Configure modifie la taille de l’objet de flux.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer :: Assets, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e0d210d7868542bf02b544c91b6f33e3ba6e5381f25462f2cfedce555858cecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016239"
---
# <a name="ibytebuffersetsize-method"></a>IByteBuffer :: deinstalle, méthode

\[La méthode **configure** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **configure** modifie la taille de l’objet de flux.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*libNewSize* \[ dans\]
</dt> <dd>

Nouvelle taille du flux sous la forme d’un nombre d’octets

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

La méthode **IByteBuffer :: configure** modifie la taille de l’objet de flux. Appelez cette méthode pour préallouer de l’espace pour le flux. Si le paramètre *libNewSize* est plus grand que la taille de flux actuelle, le flux est étendu à la taille indiquée en remplissant l’espace intermédiaire avec des octets de valeur non définie. Cette opération est semblable à la méthode [**IByteBuffer :: Write**](ibytebuffer-write.md) si le pointeur de recherche se trouve au-delà de la fin de flux actuelle.

Si le paramètre *libNewSize* est plus petit que le flux actuel, le flux est tronqué à la taille indiquée.

Le pointeur de recherche n’est pas affecté par la modification de la taille du flux.

L’appel de **IByteBuffer :: assets** peut être un moyen efficace d’obtenir un grand bloc d’espace contigu.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la définition de la taille de la mémoire tampon.


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
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



 


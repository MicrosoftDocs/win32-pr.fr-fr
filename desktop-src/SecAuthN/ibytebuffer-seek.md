---
description: La méthode Seek remplace le pointeur de recherche par un nouvel emplacement relatif au début de la mémoire tampon, à la fin de la mémoire tampon ou au pointeur de recherche actuel.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer :: Seek, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867870"
---
# <a name="ibytebufferseek-method"></a>IByteBuffer :: Seek, méthode

\[La méthode **Seek** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Seek** remplace le pointeur de recherche par un nouvel emplacement relatif au début de la mémoire tampon, à la fin de la mémoire tampon ou au pointeur de recherche actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dlibMove* \[ dans\]
</dt> <dd>

Déplacement à ajouter à l’emplacement indiqué par *dwOrigin*. Si *dwOrigin* est \_ défini pour la recherche de flux \_ , il est interprété comme une valeur non signée plutôt que comme étant signé.

</dd> <dt>

*dwOrigin* \[ dans\]
</dt> <dd>

Spécifie l’origine du déplacement spécifié dans *dlibMove*. L’origine peut être l’une des valeurs du tableau suivant.



| Valeur                                                                                                                                                                | Signification                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**\_jeu de recherche de flux \_**</dt> </dl> | Le nouveau pointeur de recherche est un décalage par rapport au début du flux. Dans ce cas, le paramètre *dlibMove* est la nouvelle position de recherche par rapport au début du flux.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**STREAM \_ Seek \_ cur**</dt> </dl> | Le nouveau pointeur de recherche est un décalage par rapport à l’emplacement du pointeur de recherche actuel. Dans ce cas, le paramètre *dlibMove* est le déplacement signé de la position de la recherche actuelle.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**fin de la recherche de flux \_ \_**</dt> </dl> | Le nouveau pointeur de recherche est un décalage par rapport à la fin du flux. Dans ce cas, le paramètre *dlibMove* est la nouvelle position de recherche par rapport à la fin du flux.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ à\]
</dt> <dd>

Pointeur vers l’emplacement où cette méthode écrit la valeur du nouveau pointeur de recherche à partir du début du flux. Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur. Dans ce cas, cette méthode ne fournit pas le nouveau pointeur de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Notes

La méthode **Seek** modifie le pointeur de recherche, de sorte que les opérations de lecture et d’écriture suivantes peuvent avoir lieu à un emplacement différent dans l’objet de flux. Il s’agit d’une erreur de recherche avant le début du flux. Toutefois, il ne s’agit pas d’une erreur de recherche au-delà de la fin du flux. La recherche au-delà de la fin du flux est utile pour les opérations d’écriture suivantes, car le flux à ce moment sera étendu à la position de recherche immédiatement avant la fin de l’opération d’écriture.

Vous pouvez également utiliser cette méthode pour obtenir la valeur actuelle du pointeur de recherche en appelant cette méthode avec le paramètre *dwOrigin* défini sur Stream \_ Seek \_ cur et le paramètre *dlibMove* défini sur zéro, de sorte que le pointeur de recherche n’est pas modifié. Le pointeur de recherche actuel est retourné dans le paramètre *plibNewPosition* .

## <a name="examples"></a>Exemples

L’exemple suivant illustre le positionnement du pointeur de recherche vers un nouvel emplacement.


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
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



 


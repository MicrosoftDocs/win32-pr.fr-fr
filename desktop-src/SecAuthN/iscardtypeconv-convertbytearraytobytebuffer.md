---
description: Convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv :: ConvertByteArrayToByteBuffer, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867838"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>ISCardTypeConv :: ConvertByteArrayToByteBuffer, méthode

\[La méthode **ConvertByteArrayToByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ConvertByteArrayToByteBuffer** convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet **IStream** ).

La mémoire tampon d’octets créée est un flux mappé sur un bloc de mémoire. Pour accéder à la mémoire tampon ou la gérer, utilisez les méthodes fournies par l’interface **IStream** . Une fonctionnalité unique de cette implémentation de tableau est que lorsque vous appelez la méthode **IStream :: Release** , la mémoire sous-jacente est libérée pour vous.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbyArray* \[ dans\]
</dt> <dd>

Pointeur vers le tableau d’octets à convertir.

</dd> <dt>

*dwArraySize* \[ dans\]
</dt> <dd>

Taille du tableau d’octets à convertir.

</dd> <dt>

*ppbyBuffer* \[ à\]
</dt> <dd>

Pointeur vers l’objet **IStream** à retourner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Mémoire allouée avec succès.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un paramètre de type pointeur était incorrect.<br/>                                            |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire libre insuffisante pour satisfaire la demande.<br/>                                            |



 

## <a name="remarks"></a>Notes

La mémoire allouée est déplaçable. Utilisez la méthode **IStream :: Release** pour libérer de la mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valeurs de retour de carte à puce](authentication-return-values.md)
</dt> </dl>

 

 

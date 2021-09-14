---
description: Convertit une mémoire tampon universelle d’octets (objet IStream) en un tableau d’octets C/C++ standard.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'ISCardTypeConv :: ConvertByteBufferToByteArray, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193855"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a>ISCardTypeConv :: ConvertByteBufferToByteArray, méthode

\[La méthode **ConvertByteBufferToByteArray** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ConvertByteBufferToByteArray** convertit une mémoire tampon universelle d’octets (objet **IStream** ) en un tableau d’octets C/C++ standard.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbyBuffer* \[ dans\]
</dt> <dd>

Pointeur vers l’objet **IStream** à convertir.

</dd> <dt>

*ppArray* \[ à\]
</dt> <dd>

Pointeur vers le tableau d’octets à retourner.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Mémoire allouée avec succès.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un paramètre de type pointeur était incorrect.<br/>                                            |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire libre insuffisante pour satisfaire la demande.<br/>                                            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
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

 

 

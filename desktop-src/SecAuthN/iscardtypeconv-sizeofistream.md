---
description: Détermine la taille, en octets, de l’interface COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv :: SizeOfIStream, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ec150fdf5a6f296b5728131cd59bb6863016fe46fe0769e6159e43b236f77a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013689"
---
# <a name="iscardtypeconvsizeofistream-method"></a>ISCardTypeConv :: SizeOfIStream, méthode

\[La méthode **SizeOfIStream** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **SizeOfIStream** détermine la taille, en octets, de l’interface com **IStream** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStrm* \[ dans\]
</dt> <dd>

Pointeur vers l’interface com **IStream** .

</dd> <dt>

*puliSize* \[ à\]
</dt> <dd>

Pointeur vers l’entier non signé long qui peut contenir l’intégralité de la valeur sizeof 64 bits de l’interface com **IStream** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi et *\* puliSize* est la taille, en octets, de l’interface com IStream.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>       | Une erreur non spécifiée s’est produite.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *puliSize* est incorrect.<br/>                                                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Le paramètre *pStrm* est incorrect.<br/>                                                          |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Une erreur inattendue s'est produite.<br/>                                                                   |



 

## <a name="requirements"></a>Configuration requise



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

 

 

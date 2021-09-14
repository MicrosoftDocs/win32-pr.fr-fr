---
description: Acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv :: GetAtIStreamMemory, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013783"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>ISCardTypeConv :: GetAtIStreamMemory, méthode

\[La méthode **GetAtIStreamMemory** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **GetAtIStreamMemory** acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface com **IStream** .

Il s’agit d’un moyen d’obtenir la mémoire sous l' **IStream** sans avoir à obtenir la valeur sizeof du bloc de mémoire en octets et à lire les octets dans un tableau d’octets temporaire à l’aide de l’interface **IStream** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStrm* \[ dans\]
</dt> <dd>

Pointeur vers l’interface com **IStream** qui gère le bloc de mémoire HGLOBAL.

</dd> <dt>

*ppMem* \[ à\]
</dt> <dd>

Pointeur vers le premier octet du bloc de mémoire HGLOBAL en cas de réussite ; Sinon, **null** si l’opération échoue.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Mémoire allouée avec succès.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un paramètre de type pointeur était incorrect.<br/>                                            |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire libre insuffisante pour satisfaire la demande.<br/>                                            |



 

## <a name="remarks"></a>Notes

Le nombre de références **IStream** sera incrémenté pour chaque pointeur *ppMem* acquis.

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

 

 

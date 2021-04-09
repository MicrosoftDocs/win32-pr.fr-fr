---
description: Crée une mémoire tampon universelle d’octets mappés à un objet IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'ISCardTypeConv :: CreateByteBuffer, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034575"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>ISCardTypeConv :: CreateByteBuffer, méthode

\[La méthode **CreateByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **CreateByteBuffer** crée une mémoire tampon universelle d’octets mappés dans un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)).

La mémoire tampon d’octets créée est un flux mappé sur un bloc de mémoire. Pour accéder à la mémoire tampon ou la gérer, utilisez les méthodes fournies par l’interface **IStream** . Une fonctionnalité unique de cette implémentation de tableau est que lorsque vous appelez la méthode **IStream :: Release** , la mémoire sous-jacente est libérée pour vous.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwAllocSize* \[ dans\]
</dt> <dd>

Taille en octets de la mémoire à allouer pour le tableau.

</dd> <dt>

*ppbyBuff* \[ à\]
</dt> <dd>

Pointeur vers l’objet IStream à retourner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Mémoire allouée avec succès.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire libre insuffisante pour satisfaire la demande.<br/>                                            |



 

## <a name="remarks"></a>Notes

La mémoire allouée est déplaçable. Utilisez la méthode **IStream :: Release** pour libérer de la mémoire.

Pour créer un tableau d’octets C/C++ classique, appelez [**CreateByteArray**](iscardtypeconv-createbytearray.md).

Pour créer un SAFEARRAY Automation de caractères non signés (octets), appelez [**CreateSafeArray**](iscardtypeconv-createsafearray.md).

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
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 

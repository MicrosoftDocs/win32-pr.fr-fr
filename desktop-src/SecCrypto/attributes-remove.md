---
description: Supprime un objet attribut indexé de la collection.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributes. Remove, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea18aab32153c998a0ddbaced65727e1ecb43dc8c54a7e3989aadcb698693970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879769"
---
# <a name="attributesremove-method"></a>Attributes. Remove, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Remove** supprime un objet [**attribut**](attribute.md) indexé de la collection.

## <a name="syntax"></a>Syntaxe


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Index de l’objet d' [**attribut**](attribute.md) à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Les applications qui utilisent cette méthode doivent contenir du code pour gérer une exception levée par cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 

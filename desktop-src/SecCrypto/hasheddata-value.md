---
description: Récupère les données hachées après des appels réussis à la méthode de hachage.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData. Value (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540949"
---
# <a name="hasheddatavalue-property"></a>HashedData. Value (propriété)

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **valeur** récupère les données hachées après des appels réussis à la méthode de [**hachage**](hasheddata-hash.md) . La valeur de hachage est retournée au format hexadécimal. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
HashedData.Value As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient les données hachées au format hexadécimal.

## <a name="remarks"></a>Notes

Pour créer le hachage d’une grande quantité de données, appelez la méthode de [**hachage**](hasheddata-hash.md) pour chaque élément de données. Le hachage de chaque élément de données est concaténé à la propriété **value** jusqu’à ce que la propriété soit lue. Le contenu de la propriété **value** est réinitialisé lorsque la propriété est lue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 

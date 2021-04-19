---
description: Récupère la collection d’attributs authentifiés.
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: Propriété signer. AuthenticatedAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537378"
---
# <a name="signerauthenticatedattributes-property"></a>Propriété signer. AuthenticatedAttributes

\[La propriété **AuthenticatedAttributes** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **AuthenticatedAttributes** récupère la collection d’attributs authentifiés.

## <a name="syntax"></a>Syntaxe


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a>Valeur de la propriété

Collection d' [**attributs**](attributes.md) qui représente les attributs authentifiés du signataire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Signataire**](signer.md)
</dt> </dl>

 

 

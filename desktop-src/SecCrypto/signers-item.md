---
description: Récupère l’objet signataire qui représente le signataire indexé.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Propriété Signers. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543366"
---
# <a name="signersitem-property"></a>Propriété Signers. Item

\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt une collection d’objets CmsSigner. Pour plus d’informations, consultez la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Item** récupère l’objet [**signataire**](signer.md) qui représente le signataire indexé. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**signataire**](signer.md) qui représente le signataire indexé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Signataires**](signers.md)
</dt> </dl>

 

 

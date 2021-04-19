---
description: Récupère un objet de la collection Recipients.
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: Destinataires. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a80b472c8257597356c626a9e88aad97c447f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532570"
---
# <a name="recipientsitem-property"></a>Destinataires. Item, propriété

\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Item** récupère un objet de la collection [**Recipients**](recipients.md) . Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Variant qui représente l’élément indexé dans la collection [**Recipients**](recipients.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Destinataires**](recipients.md)
</dt> </dl>

 

 

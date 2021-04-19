---
description: Définit ou récupère les données à signer. Il s’agit de la propriété par défaut.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540063"
---
# <a name="signeddatacontent-property"></a>SignedData. Content, propriété

\[La propriété **contenu** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété de **contenu** définit ou récupère les données à signer. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Valeur de la propriété

Données à signer.

## <a name="remarks"></a>Notes

Cette propriété doit être initialisée avant l’appel de la méthode [**Sign**](signeddata-sign.md) . Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée, et toute signature associée à l’objet avant la modification de la propriété est perdue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

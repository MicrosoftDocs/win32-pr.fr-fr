---
description: Récupère les créateurs de signature des données.
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: SignedData. Signers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532748"
---
# <a name="signeddatasigners-property"></a>SignedData. Signers, propriété

\[La propriété des **signataires** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété des **signataires** récupère les créateurs de signature des données.

## <a name="syntax"></a>Syntaxe


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a>Valeur de la propriété

Collection de [**signataires**](signers.md) qui représente les créateurs de signature des données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

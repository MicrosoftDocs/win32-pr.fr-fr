---
description: Récupère l’algorithme de chiffrement et la longueur de clé.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData. algorithme, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525470"
---
# <a name="envelopeddataalgorithm-property"></a>EnvelopedData. algorithme, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **algorithme** récupère l’algorithme de chiffrement et la [*longueur de clé*](../secgloss/k-gly.md).

## <a name="syntax"></a>Syntaxe


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**algorithme**](algorithm.md) qui contient l’algorithme de chiffrement et la longueur de clé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 

---
description: La propriété Certificates récupère une collection de certificats qui représente les certificats dans la chaîne. Il s’agit de la propriété par défaut.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2 :: Certificates, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528085"
---
# <a name="ichain2certificates-property"></a>IChain2 :: Certificates, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Certificates** récupère une collection de [**certificats**](certificates.md) qui représente les certificats dans la chaîne. Il s’agit de la propriété par défaut.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Valeur de la propriété

Collection de [**certificats**](certificates.md) utilisée pour récupérer des informations sur chaque certificat dans la chaîne. Le premier certificat de la collection retournée, Certificates **. Item**(1), est le certificat de fin de la chaîne. Le dernier certificat de la collection, Certificates **. Item**(**Certificates. Count**), est le [*certificat racine*](../secgloss/r-gly.md) de la chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

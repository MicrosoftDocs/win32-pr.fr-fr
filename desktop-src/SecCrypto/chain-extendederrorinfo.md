---
description: Retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'IChain2 :: ExtendedErrorInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522810"
---
# <a name="ichain2extendederrorinfo-method"></a>IChain2 :: ExtendedErrorInfo, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **ExtendedErrorInfo** retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.

Cette méthode est introduite dans CAPICOM 2,0.

## <a name="syntax"></a>Syntaxe


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans, facultatif\]
</dt> <dd>

**Valeur de type long** représentant l’index de l’entrée. La valeur par défaut est 1, qui retourne des informations d’erreur pour le certificat de fin dans la chaîne. Certificates **. Count** retourne des informations sur le certificat racine de la chaîne. 0 retourne des informations d’erreur étendues pour la chaîne entière.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne qui contient les informations d’erreur étendues.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Mutation**](chain.md)
</dt> </dl>

 

 

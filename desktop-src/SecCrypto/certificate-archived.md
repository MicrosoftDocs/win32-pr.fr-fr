---
description: Définit ou récupère une valeur booléenne qui indique si le certificat est archivé.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Propriété Certificate. Archived
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771948"
---
# <a name="certificatearchived-property"></a>Propriété Certificate. Archived

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **archivée** définit ou récupère une valeur booléenne qui indique si le certificat est archivé.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique si le certificat est archivé. Si la **valeur est true**, le certificat est archivé. Notez que le fait de remplacer la valeur **false** par **true** Archive le certificat.

## <a name="remarks"></a>Remarques

Cette propriété déclenche l’E CAPICOM \_ E \_ non \_ autorisée lorsque le script est basé sur une application Web.

> [!Note]  
> Un certificat archivé n’est pas visible dans l’interface utilisateur de gestion des certificats. En outre, les certificats archivés ne sont pas inclus dans la méthode [**Store. Open**](store-open.md) sauf si le \_ magasin CAPICOM \_ Open \_ include \_ est spécifié.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

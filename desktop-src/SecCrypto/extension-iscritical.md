---
description: Récupère une valeur booléenne qui indique si l’extension est marquée comme critique.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Propriété extension. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526033"
---
# <a name="extensioniscritical-property"></a>Propriété extension. IsCritical

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension est marquée comme critique.

## <a name="syntax"></a>Syntaxe


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension est marquée comme critique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

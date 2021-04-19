---
description: Récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Propriété Template. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539681"
---
# <a name="templateiscritical-property"></a>Propriété Template. IsCritical

\[La propriété **IsCritical** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]

La propriété **IsCritical** récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.

## <a name="syntax"></a>Syntaxe


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension de modèle est marquée comme critique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modèle**](template.md)
</dt> </dl>

 

 

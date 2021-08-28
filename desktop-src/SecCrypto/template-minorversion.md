---
description: Récupère le numéro de version mineure du modèle.
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: Template. MinorVersion, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 695bde72274f9fe1e6df6e77eed1f956052a46201ae4be10e0848e8285cfa3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897404"
---
# <a name="templateminorversion-property"></a>Template. MinorVersion, propriété

\[La propriété **MinorVersion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]

La propriété **MinorVersion** récupère le numéro de version mineure du modèle.

## <a name="syntax"></a>Syntaxe


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de version mineure du modèle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modèle**](template.md)
</dt> </dl>

 

 

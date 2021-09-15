---
description: Fournit un accès en lecture seule aux propriétés d’utilisation de la clé d’un certificat.
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: Objet KeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d2324b4e1e06650f2eed7b63337f2bd48520498
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413459"
---
# <a name="keyusage-object"></a>Objet KeyUsage

\[L’objet **KeyUsage** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **KeyUsage** fournit un accès en lecture seule aux propriétés d’utilisation de la clé d’un certificat.

## <a name="members"></a>Membres

L’objet **KeyUsage** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **KeyUsage** possède ces propriétés.



| Propriété                                                                           | Type d’accès          | Description                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension **KeyUsage** est marquée comme critique.<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit bit cRLSign est défini.<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit dataEncipherment est défini.<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit decipherOnly est défini.<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit digitalSignature est défini.<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit encipherOnly est défini.<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit keyAgreement est défini.<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit bit keyCertSign est défini.<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit keyEncipherment est défini.<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | Lecture seule<br/> | Récupère une valeur booléenne qui indique si le bit nonRepudiationEnabled est défini.<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension **KeyUsage** est présente.<br/> Il s’agit de la propriété par défaut.<br/> |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **KeyUsage** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 

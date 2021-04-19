---
description: Représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Qualificateur (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525495"
---
# <a name="qualifier-object"></a>Qualificateur (objet)

\[L’objet **qualificateur** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

L’objet **qualificateur** représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **qualificateur** est utilisé pour effectuer les tâches suivantes :

-   Récupérez l’identificateur d’objet du qualificateur.
-   Récupérez le Uniform Resource Identifier (URI) qui pointe vers un CPS publié par l' [*autorité de certification*](../secgloss/c-gly.md) .
-   Récupérez le nom de l’organisation associée au qualificateur.
-   Récupérez le nom et le contenu d’une notification utilisateur.

## <a name="members"></a>Membres

L’objet **qualificateur** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **qualificateur** a ces propriétés.



| Propriété                                                          | Type d’accès          | Description                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Lecture seule<br/> | Récupère une chaîne qui contient l’URI qui pointe vers un CPS publié par l’autorité de certification.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Lecture seule<br/> | Récupère une chaîne qui contient le contenu de l’avis de l’utilisateur. Cette propriété peut être vide.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Lecture seule<br/> | Récupère un objet **NoticeNumbers** qui contient la collection de numéros d’avis d’utilisateur. Cette propriété peut être vide.<br/>    |
| [**OID**](qualifier-oid.md)<br/>                           | Lecture seule<br/> | Récupère un objet [**OID**](oid.md) qui identifie le qualificateur. Il s’agit de la propriété par défaut.<br/>                      |
| [**Morgan**](qualifier-organizationname.md)<br/> | Lecture seule<br/> | Récupère une chaîne qui contient le nom de l’organisation associée au qualificateur. Cette propriété peut être vide.<br/> |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **qualificateur** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

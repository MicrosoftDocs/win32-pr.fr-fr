---
description: Collection d’objets PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objet CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542579"
---
# <a name="certificatepolicies-object"></a>Objet CertificatePolicies

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]

L’objet **certificatePolicies** représente une collection d’objets [**PolicyInformation**](policyinformation.md) . Chaque objet [**PolicyInformation**](policyinformation.md) représente une stratégie de certificat unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **certificatePolicies** est utilisé pour effectuer les tâches suivantes :

-   Récupérez le nombre de stratégies de certificat dans la collection.
-   Récupérez un objet [**PolicyInformation**](policyinformation.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **certificatePolicies** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **certificatePolicies** a ces propriétés.



| Propriété                                                    | Type d’accès          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](certificatepolicies-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection.<br/>                                                                                                                    |
| [**Élément**](certificatepolicies-item.md)<br/>         | Lecture seule<br/> | Récupère un objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie de certificat indexée de la collection. Il s’agit de la propriété par défaut.<br/>                                                    |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **certificatePolicies** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

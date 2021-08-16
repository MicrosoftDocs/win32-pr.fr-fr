---
description: Représente une collection de qualificateurs.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualificateurs, objet (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f68dbeefefbe675199522dfbc5b1dab81b8a2840fa8b7d5189c72b811fcba7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900955"
---
# <a name="qualifiers-object"></a>Qualificateurs, objet

\[L’objet **qualificateurs** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

L’objet **qualificateurs** représente une collection de qualificateurs.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **qualificateurs** est utilisé pour effectuer les tâches suivantes :

-   Récupère une propriété étendue spécifique de la collection.
-   Récupérez le nombre de propriétés étendues dans la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **qualificateurs** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **qualificateurs** possède ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](qualifiers-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre de qualificateurs dans la collection.<br/>                                                                                                                                                                |
| [**Élément**](qualifiers-item.md)<br/>         | Lecture seule<br/> | Récupère un objet [**qualificateur**](qualifier.md) qui représente le qualificateur indexé de la collection. Il s’agit de la propriété par défaut.<br/>                                                                             |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **qualificateurs** .

La propriété d’objet [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) CAPICOM retourne un objet **qualificateurs** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| En-tête<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

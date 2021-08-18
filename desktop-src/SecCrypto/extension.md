---
description: Représente une extension de certificat unique.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objet d’extension (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e311c6dc69f40d32163c70cabf6a38780a989764bd77f4023c61ede5c1ba713c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006957"
---
# <a name="extension-object"></a>Objet d’extension

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet d' **extension** représente une extension de certificat unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet d' **extension** est utilisé pour effectuer les tâches suivantes :

-   Récupérez l’OID de l’extension de certificat.
-   Récupérer les données d’extension de certificat représentées par un objet [**EncodedData**](encodeddata.md) .
-   Déterminez si l’extension de certificat est marquée comme critique.

## <a name="members"></a>Membres

L’objet d' **extension** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet d' **extension** possède ces propriétés.



| Propriété                                                | Type d’accès          | Description                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Lecture seule<br/> | Récupère les données encodées pour l’extension.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension est marquée comme critique.<br/> |
| [**OID**](extension-oid.md)<br/>                 | Lecture seule<br/> | Récupère l’identificateur d’objet pour l’extension. Il s’agit de la propriété par défaut.<br/>   |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet d' **extension** .

L’objet d' **extension** est utilisé par l’objet de collection d' [**Extensions**](extensions.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| En-tête<br/>                | <dl> <dt>Mmcobj. h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

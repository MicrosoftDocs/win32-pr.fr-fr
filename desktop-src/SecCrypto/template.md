---
description: Représente le modèle d’extension de certificat du certificat.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objet de modèle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897320"
---
# <a name="template-object"></a>Objet de modèle

\[L’objet **modèle** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]

L’objet **modèle** représente le modèle d’extension de certificat du certificat.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet de **modèle** est utilisé pour effectuer les tâches suivantes :

-   Déterminez si le modèle est marqué comme critique ou présent.
-   Récupérez l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) ou le nom du modèle.
-   Récupérez la version mineure ou majeure du modèle.

## <a name="members"></a>Membres

L’objet de **modèle** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet de **modèle** a ces propriétés.



| Propriété                                                 | Type d’accès          | Description                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension de modèle est marquée comme critique.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Lecture seule<br/> | Récupère une valeur booléenne qui indique si l’extension de modèle est présente.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Lecture seule<br/> | Récupère le numéro de version principale du modèle.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Lecture seule<br/> | Récupère le numéro de version mineure du modèle.<br/>                                         |
| [**Nom**](template-name.md)<br/>                 | Lecture seule<br/> | Récupère une chaîne qui contient le nom du modèle.<br/>                                  |
| [**OID**](template-oid.md)<br/>                   | Lecture seule<br/> | Récupère un objet [**OID**](oid.md) qui identifie l’objet de **modèle** .<br/>             |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet de **modèle** .

Un objet **modèle** est retourné par la méthode [**Certificate. Template**](certificate-template.md) .

CAPICOM utilise deux versions différentes de modèles de certificats. Le tableau suivant indique le nom et l’OID de chaque version de modèle de certificat.



| Version | Nom                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | EXTENSION szOID d' \_ inscription \_ le type \_ | "1.3.6.1.4.1.311.20.2" |
| V2      | \_modèle de certificat szOID \_       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

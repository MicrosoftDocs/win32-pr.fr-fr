---
description: Fournit des fonctionnalités pour la signature des fichiers exécutables avec une signature numérique Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objet SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e119a639af7cb6459e8e6ec8ae6416f9d067c56e8f81560fedc385abd518b840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899338"
---
# <a name="signedcode-object"></a>Objet SignedCode

\[L’objet **SignedCode** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

L’objet **SignedCode** fournit des fonctionnalités pour la signature des fichiers exécutables avec une signature numérique Authenticode.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **SignedCode** est utilisé pour effectuer les tâches suivantes :

-   Signez les fichiers exécutables.
-   Horodatage des fichiers exécutables.
-   Déterminez si la signature du fichier exécutable est valide.
-   Définissez ou récupérez le chemin d’accès au fichier exécutable.
-   Récupérez le signataire et la matrice temporelle du fichier exécutable.
-   Récupérez une collection de certificats pour le fichier exécutable.
-   Récupérez une description ou l’URL de la description du fichier exécutable.

## <a name="members"></a>Membres

L’objet **SignedCode** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SignedCode** a ces méthodes.



| Méthode                                    | Description                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Expéditeur**](signedcode-sign.md)           | Crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .<br/> |
| [**Vérification**](signedcode-verify.md)       | Vérifie la signature Authenticode sur le fichier exécutable signé spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .<br/>          |



 

### <a name="properties"></a>Propriétés

L’objet **SignedCode** a ces propriétés.



| Propriété                                                       | Type d’accès           | Description                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificats**](signedcode-certificates.md)<br/>     | Lecture seule<br/>  | Collection de [**certificats**](certificates.md) qui contient tous les certificats dans le fichier exécutable signé.<br/>             |
| [**Description**](signedcode-description.md)<br/>       | Lecture/écriture<br/> | Chaîne qui contient une description du fichier exécutable signé.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lecture/écriture<br/> | Chaîne qui contient l’adresse HTTP à une description du fichier exécutable signé.<br/>                                         |
| [**Extension**](signedcode-filename.md)<br/>             | Lecture/écriture<br/> | Chaîne qui contient le chemin d’accès au fichier de contenu qui contient le fichier exécutable.<br/> Il s’agit de la propriété par défaut.<br/> |
| [**Signataire**](signedcode-signer.md)<br/>                 | Lecture seule<br/>  | Objet [**signataire**](signer.md) qui fournit l’accès au signataire du fichier exécutable.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Lecture seule<br/>  | Objet [**signataire**](signer.md) qui fournit l’accès à l’horodatage du fichier exécutable.<br/>                              |



 

## <a name="remarks"></a>Remarques

L’objet **SignedCode** peut être créé et n’est pas sûr pour l’écriture de scripts. Le ProgID de l’objet **SignedCode** est CAPICOM. SignedCode. 1.

Le fichier exécutable doit être d’un type qui peut être signé avec la technologie Authenticode, par exemple, les fichiers ayant l’extension de nom de fichier .cab,. cat, .exe, .dll,. vbs ou. ocx.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

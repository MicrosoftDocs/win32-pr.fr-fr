---
description: Fournit des propriétés et des méthodes permettant d’établir le contenu à signer à l’aide d’une signature numérique, de signer ou de signer des données numériquement, et de vérifier la signature numérique des données signées. Le message signé est au \# format PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objet SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ec8d4b874f9269e4850b87ad65aab52563d007c805924bb0ab83f9ce76f8f38e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973721"
---
# <a name="signeddata-object"></a>Objet SignedData

\[L’objet **SignedData** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **SignedData** fournit des propriétés et des méthodes permettant d’établir le contenu à signer à l’aide d’une [*signature numérique*](../secgloss/d-gly.md), de signer ou de signer des données numériquement, et de vérifier la signature numérique des données signées. Le message signé est au \# format PKCS 7.

Une signature de données, si elle est vérifiée, prouve l’association entre un signataire et des données et indique que les données n’ont pas été modifiées après la création de la signature.

## <a name="members"></a>Membres

L’objet **SignedData** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SignedData** a ces méthodes.



| Méthode                              | Description                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**Cosigne**](signeddata-cosign.md) | Cosigne un message déjà signé.<br/>                       |
| [**Expéditeur**](signeddata-sign.md)     | Crée une signature numérique sur le contenu à signer.<br/> |
| [**Vérifier**](signeddata-verify.md) | Détermine la validité d’une signature ou de signatures.<br/>    |



 

### <a name="properties"></a>Propriétés

L’objet **SignedData** a ces propriétés.



| Propriété                                                   | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificats**](signeddata-certificates.md)<br/> | Lecture seule<br/>  | Récupère la collection de [**certificats**](certificates.md) des données signées.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Content**](signeddata-content.md)<br/>           | Lecture/écriture<br/> | Données à signer. Cette propriété doit être initialisée avant l’appel de la méthode [**Sign**](signeddata-sign.md) .<br/> Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée, et toute signature associée à l’objet avant la modification de la propriété est perdue.<br/> Il s’agit de la propriété par défaut.<br/> |
| [**Signataires**](signeddata-signers.md)<br/>           | Lecture seule<br/>  | Récupère la collection de [**signataires**](signers.md) qui représente les créateurs de signature des données.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Remarques

L’objet **SignedData** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **SignedData** est CAPICOM. SignedData. 1.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 

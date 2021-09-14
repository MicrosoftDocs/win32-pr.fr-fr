---
description: Représente un bloc de données encodées ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objet EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416452"
---
# <a name="encodeddata-object"></a>Objet EncodedData

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **EncodedData** représente un bloc de données encodées ASN. 1.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **EncodedData** est retourné par plusieurs propriétés de l’objet CAPICOM. Une fois retourné, cet objet est utilisé pour effectuer les tâches suivantes :

-   Obtient une représentation sous forme de chaîne des données encodées.
-   Obtenez l’objet décodeur, s’il existe, qui est associé aux données encodées.
-   Déterminez le type de données encodées.

## <a name="members"></a>Membres

L’objet **EncodedData** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **EncodedData** a ces méthodes.



| Méthode                                 | Description                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Décodeur**](encodeddata-decoder.md) | Obtient un objet décodeur, s’il en existe un.<br/>             |
| [**Format**](encodeddata-format.md)   | Retourne une représentation sous forme de chaîne des données encodées.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **EncodedData** a ces propriétés.



| Propriété                                      | Type d’accès          | Description                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Valeur**](encodeddata-value.md)<br/> | Lecture seule<br/> | Récupère les données encodées. Il s’agit de la propriété par défaut.<br/> |



 

## <a name="remarks"></a>Notes

Le seul type de données encodées pris en charge est [**certificatePolicies**](certificatepolicies.md).

Impossible de créer l’objet **EncodedData** .

Les propriétés suivantes de l’objet CAPICOM retournent un objet **EncodedData** :

-   **PublicKey. EncodedKey**
-   **PublicKey. EncodedParameters**
-   **Extension. EncodedData**
-   **Policy. EncodedData**

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

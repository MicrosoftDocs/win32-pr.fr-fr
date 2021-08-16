---
description: L’objet EnvelopedData fournit des propriétés et des méthodes pour encapsuler les données en vue de leur confidentialité par chiffrement.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objet EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: af88fd9b4be0c7ddd9fe5dfc204558c1a36cab418166f73c8de0ec0c06c0a8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766110"
---
# <a name="envelopeddata-object"></a>Objet EnvelopedData

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **EnvelopedData** fournit des propriétés et des méthodes pour encapsuler les données en vue de leur confidentialité par chiffrement. Pour encapsuler des données, une clé de chiffrement de session est générée. Cette [*clé de session*](../secgloss/s-gly.md) est ensuite chiffrée pour chaque destinataire prévu à l’aide de la [*clé publique*](../secgloss/p-gly.md) de ce destinataire prévu du certificat du destinataire. Les données chiffrées et l’ensemble des clés de session chiffrées peuvent être envoyés à tous les destinataires prévus. Le message généré est au \# format PKCS 7.

## <a name="members"></a>Membres

L’objet **EnvelopedData** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **EnvelopedData** a ces méthodes.



| Méthode                                   | Description                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Crypté**](envelopeddata-decrypt.md) | Déchiffre le contenu enveloppé.<br/>                                                                      |
| [**Encrypt**](envelopeddata-encrypt.md) | Chiffre le contenu, chiffre une clé de session pour chaque destinataire et retourne l’objet BLOB chiffré.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **EnvelopedData** a ces propriétés.



| Propriété                                                  | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithm**](envelopeddata-algorithm.md)<br/>   | Lecture/écriture<br/> | Algorithme de chiffrement et [*longueur de clé*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Content**](envelopeddata-content.md)<br/>       | Lecture/écriture<br/> | Contenu en texte clair d’un message à envelopper. La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](envelopeddata-encrypt.md) .<br/> Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.<br/> Il s’agit de la propriété par défaut.<br/> |
| [**Destinataires**](envelopeddata-recipients.md)<br/> | Lecture seule<br/>  | Collection d’objets de [**certificat**](certificate.md) pour recevoir le message enveloppé.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Remarques

L’objet **EnvelopedData** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **EnvelopedData** est CAPICOM. EnvelopedData. 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 

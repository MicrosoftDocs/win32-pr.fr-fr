---
description: Fournit des fonctionnalités pour la génération de nombres aléatoires, les conversions et l’encodage et le décodage à partir de base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objet Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540614"
---
# <a name="utilities-object"></a>Objet Utilities

\[L’objet **Utilities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]

L’objet **Utilities** fournit des fonctionnalités pour la génération de nombres aléatoires, les conversions et l’encodage et le décodage à partir de base64.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **Utilities** est utilisé pour effectuer les tâches suivantes :

-   Encoder une chaîne en base64 ou décoder une chaîne de base64.
-   Convertit une chaîne binaire compressée en un tableau d’octets, et vice versa.
-   Convertit une chaîne binaire compressée en chaîne hexadécimale, et vice versa.
-   Générez un nombre aléatoire sécurisé.
-   Convertit l’heure locale en temps universel coordonné (heure de Greenwich) et vice versa.

## <a name="members"></a>Membres

L’objet **Utilities** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **Utilities** possède ces méthodes.



| Méthode                                                               | Description                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | Décode une chaîne de base64.<br/>                                     |
| [**Base64Encode**](utilities-base64encode.md)                       | Encode une chaîne au format Base64.<br/>                                       |
| [**BinaryStringToByteArray**](utilities-binarystringtobytearray.md) | Convertit une chaîne binaire compressée en un tableau d’octets.<br/>             |
| [**BinaryToHex**](utilities-binarytohex.md)                         | Convertit une chaîne binaire compressée en chaîne hexadécimale.<br/>          |
| [**ByteArrayToBinaryString**](utilities-bytearraytobinarystring.md) | Convertit un tableau d’octets en une chaîne condensé binaire.<br/>             |
| [**GetRandom**](utilities-getrandom.md)                             | Génère un nombre aléatoire sécurisé.<br/>                                 |
| [**HexToBinary**](utilities-hextobinary.md)                         | Convertit une chaîne hexadécimale en chaîne binaire.<br/>          |
| [**LocalTimeToUTCTime**](utilities-localtimetoutctime.md)           | Convertit l’heure locale de l’ordinateur en temps universel coordonné.<br/> |
| [**UTCTimeToLocalTime**](utilities-utctimetolocaltime.md)           | Convertit le temps universel coordonné en heure locale de l’ordinateur.<br/> |



 

## <a name="remarks"></a>Notes

L’objet **Utilities** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **Utilities** est CAPICOM. Utilities. 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 





---
title: EAPHost et schéma hérité
description: Décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381275"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost et schéma hérité

Cette rubrique décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML.

## <a name="about-eaphost-and-legacy-schema"></a>À propos de EAPHost et du schéma hérité

La création du fichier XML de configuration commence avec le schéma [eaphostconfig](eaphostconfigschema-schema.md) ; la création d’informations d’identification XML commence par le schéma [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .

Plusieurs schémas natif et hérité contiennent des éléments de schéma communs. Les éléments communs utilisés dans la configuration de méthode et les informations d’identification de méthode sont abstraits dans un fichier de schéma unique, appelé « schéma commun ».

Les termes « configuration de la méthode » et « propriétés de connexion » sont utilisés indifféremment. De même, les termes « informations d’identification de la méthode » et « propriétés de l’utilisateur » sont également utilisés indifféremment.

## <a name="eaphost-schema"></a>Schéma EAPHost



| schéma                                                                        | Description                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | Contient des éléments de schéma de configuration communs.     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | Contient des éléments de schéma d’informations d’identification courants.        |
| [eapcommon](eapcommonschema-schema.md)                                       | Contient la définition de l’élément **EapMethodType** . |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | Contient le schéma de configuration EAPHost.             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | Contient le schéma des informations d’identification EAPHost.                |



 

## <a name="legacy-schema"></a>Schéma hérité



| schéma                                                                            | Description                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | Contient des éléments de schéma de configuration communs.                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | Contient des éléments de schéma d’informations d’identification courants.                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | Contient des éléments de schéma de configuration communs.                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | Contient des éléments de schéma d’informations d’identification courants.                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | Est utilisé avec EAP-TLS pour décrire les données de configuration de l’authentification.                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | Est utilisé avec EAP-TLS pour décrire les données de configuration d’authentification à partir de Windows 7. |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | Est utilisé avec EAP-TLS pour décrire les informations d’identification d’authentification et les options d’informations d’identification.          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | Est utilisé avec MS-CHAPv2 pour décrire les données de configuration de l’authentification.                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | Est utilisé avec MS-CHAPv2 pour décrire les informations d’identification d’authentification et les options d’informations d’identification.        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | Est utilisé avec PEAPv0 pour décrire les données de configuration de l’authentification.                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | Est utilisé avec PEAPv0 pour décrire les données de configuration d’authentification à partir de Windows 7.  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | Est utilisé avec PEAPv0 pour décrire les informations d’identification d’authentification et les options d’informations d’identification.           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Examen des exemples de schéma EAPHost et hérité](eaphost-schemas.md)
</dt> </dl>

 

 





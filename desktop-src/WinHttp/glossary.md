---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: Glossaire (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866229"
---
# <a name="glossary-winhttp"></a>Glossaire (WinHTTP)

<dl> <dt>

<span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**données d’authentification**
</dt> <dd>

Bloc de données spécifique au schéma qui est échangé entre le serveur et le client lors de l’authentification. Pour prouver son identité, le client chiffre une partie ou l’ensemble de ces données avec un nom d’utilisateur et un mot de passe. Le client envoie les données chiffrées au serveur, qui déchiffre les données et les compare à l’original. Si les données déchiffrées correspondent aux données d’origine, le client est authentifié.

</dd> <dt>

<span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**encodage Base64**
</dt> <dd>

Schéma utilisé pour transmettre des données binaires. Base64 traite les données en tant que groupes 24 bits, en mappant ces données à quatre caractères encodés. Il est parfois désigné sous le terme de « codage 3 à 4 ». Chaque 6 bits du groupe 24 bits est utilisé comme index dans une table de mappage (l’alphabet base64) pour obtenir un caractère pour les données encodées. Les données encodées ont des longueurs de ligne limitées à 76 caractères.

</dd> <dt>

<span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**magasin de certificats**
</dt> <dd>

En général, stockage permanent dans lequel les certificats, les listes de révocation de certificats (CRL) et les listes de certificats de confiance (CTL) sont stockés. Un magasin de certificats peut également être temporaire lors de l’utilisation de certificats basés sur une session.

</dd> <dt>

<span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**
</dt> <dd>

Possibilité pour un site Microsoft Passport participant de fournir ses propres éléments de personnalisation et des explications sur les pages de service réseau Passport. La copersonnalisation comprend la personnalisation de l’apparence, du texte spécifique et du comportement spécifique sur les pages réseau Passport.

</dd> <dt>

<span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**page de codes**
</dt> <dd>

Table qui lie les codes de caractères binaires utilisés par un programme aux touches du clavier ou à l’apparence des caractères sur l’analyse. L’utilisation de pages de codes est un moyen de prendre en charge les jeux de caractères et les dispositions de clavier utilisés dans différents pays et régions. Vous pouvez configurer des appareils tels que l’analyseur et le clavier pour utiliser une page de codes spécifique et passer d’une page de codes (telle que États-Unis) à une autre (par exemple, le Portugal) à la demande de l’utilisateur.

</dd> <dt>

<span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbe HTTP**
</dt> <dd>

Le verbe HTTP (ou la méthode HTTP) est une instruction envoyée dans un message de demande qui notifie un serveur HTTP de l’action à effectuer sur la ressource spécifiée. Par exemple, « obtenir » indique qu’une ressource est récupérée à partir du serveur. LES verbes courants incluent « obtient », « poster » et « HEAD ». Pour plus d’informations et pour obtenir la liste complète des verbes HTTP standard, consultez la spécification HTTP/1.1.

</dd> <dt>

<span id="term_ticket"></span><span id="TERM_TICKET"></span>**titre**
</dt> <dd>

Cookie qui contient un profil utilisateur pour l’authentification Passport. Chaque ticket correspond à une URL. Le serveur d’ouverture de session d’une autorité de domaine Passport fournit des tickets que le client envoie à un membre Passport pour l’authentification.

</dd> <dt>

<span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agent utilisateur**
</dt> <dd>

L’agent utilisateur est l’application cliente qui demande un document à partir d’un serveur HTTP. Lorsque le client envoie une demande à un serveur HTTP, il envoie généralement le nom de l’agent utilisateur avec l’en-tête de demande afin que le serveur puisse déterminer les fonctionnalités du logiciel client.

</dd> </dl>

 

 




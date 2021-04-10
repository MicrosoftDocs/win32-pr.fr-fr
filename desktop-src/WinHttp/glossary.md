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
# <a name="glossary-winhttp"></a><span data-ttu-id="5d4c8-103">Glossaire (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="5d4c8-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="5d4c8-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**données d’authentification**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-105">Bloc de données spécifique au schéma qui est échangé entre le serveur et le client lors de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="5d4c8-106">Pour prouver son identité, le client chiffre une partie ou l’ensemble de ces données avec un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="5d4c8-107">Le client envoie les données chiffrées au serveur, qui déchiffre les données et les compare à l’original.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="5d4c8-108">Si les données déchiffrées correspondent aux données d’origine, le client est authentifié.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**encodage Base64**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-110">Schéma utilisé pour transmettre des données binaires.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="5d4c8-111">Base64 traite les données en tant que groupes 24 bits, en mappant ces données à quatre caractères encodés.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="5d4c8-112">Il est parfois désigné sous le terme de « codage 3 à 4 ».</span><span class="sxs-lookup"><span data-stu-id="5d4c8-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="5d4c8-113">Chaque 6 bits du groupe 24 bits est utilisé comme index dans une table de mappage (l’alphabet base64) pour obtenir un caractère pour les données encodées.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="5d4c8-114">Les données encodées ont des longueurs de ligne limitées à 76 caractères.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**magasin de certificats**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-116">En général, stockage permanent dans lequel les certificats, les listes de révocation de certificats (CRL) et les listes de certificats de confiance (CTL) sont stockés.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="5d4c8-117">Un magasin de certificats peut également être temporaire lors de l’utilisation de certificats basés sur une session.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-119">Possibilité pour un site Microsoft Passport participant de fournir ses propres éléments de personnalisation et des explications sur les pages de service réseau Passport.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="5d4c8-120">La copersonnalisation comprend la personnalisation de l’apparence, du texte spécifique et du comportement spécifique sur les pages réseau Passport.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**page de codes**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-122">Table qui lie les codes de caractères binaires utilisés par un programme aux touches du clavier ou à l’apparence des caractères sur l’analyse.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="5d4c8-123">L’utilisation de pages de codes est un moyen de prendre en charge les jeux de caractères et les dispositions de clavier utilisés dans différents pays et régions.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="5d4c8-124">Vous pouvez configurer des appareils tels que l’analyseur et le clavier pour utiliser une page de codes spécifique et passer d’une page de codes (telle que États-Unis) à une autre (par exemple, le Portugal) à la demande de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**Verbe HTTP**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-126">Le verbe HTTP (ou la méthode HTTP) est une instruction envoyée dans un message de demande qui notifie un serveur HTTP de l’action à effectuer sur la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="5d4c8-127">Par exemple, « obtenir » indique qu’une ressource est récupérée à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="5d4c8-128">LES verbes courants incluent « obtient », « poster » et « HEAD ».</span><span class="sxs-lookup"><span data-stu-id="5d4c8-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="5d4c8-129">Pour plus d’informations et pour obtenir la liste complète des verbes HTTP standard, consultez la spécification HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**titre**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-131">Cookie qui contient un profil utilisateur pour l’authentification Passport.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="5d4c8-132">Chaque ticket correspond à une URL.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="5d4c8-133">Le serveur d’ouverture de session d’une autorité de domaine Passport fournit des tickets que le client envoie à un membre Passport pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5d4c8-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**agent utilisateur**</span><span class="sxs-lookup"><span data-stu-id="5d4c8-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="5d4c8-135">L’agent utilisateur est l’application cliente qui demande un document à partir d’un serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="5d4c8-136">Lorsque le client envoie une demande à un serveur HTTP, il envoie généralement le nom de l’agent utilisateur avec l’en-tête de demande afin que le serveur puisse déterminer les fonctionnalités du logiciel client.</span><span class="sxs-lookup"><span data-stu-id="5d4c8-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 




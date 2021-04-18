---
title: Forum aux questions (FAQ)
description: Lisez les réponses aux questions les plus fréquemment posées sur les API EAPHost, telles que « qu’est-ce que la durée de vie d’une authentification ? ».
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106529069"
---
# <a name="general-frequently-asked-questions"></a>Forum aux questions (FAQ)

La rubrique suivante fournit des réponses aux questions fréquemment posées sur les API EAPHost.

### <a name="general-frequently-asked-questions"></a>Forum aux questions (FAQ)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Question</th>
<th>Réponse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Qu’est-ce qu’un demandeur ?</td>
<td>Le demandeur est l’entité à authentifier à l’aide d’EAPHost. Les demandeurs classiques sont les clients [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , les clients 802,3 et le service Routage et accès à distance (RRAS), clients point-à-point (PPP).</td>
</tr>
<tr class="even">
<td>Qu’est-ce qu’un homologue ?</td>
<td>L’homologue est le côté client d’une authentification EAP.</td>
</tr>
<tr class="odd">
<td>Quelle est la différence entre un homologue et un demandeur ?</td>
<td>Le demandeur transporte les paquets, contrairement à un homologue. Néanmoins, les termes homologue, demandeur et client sont en grande partie synonymes.</td>
</tr>
<tr class="even">
<td>Qu’est-ce qu’un authentificateur ?</td>
<td>L’authentificateur est le point d’accès sans fil, le serveur d’accès réseau (NAS) ou le périphérique d’accès au réseau (NAD) qui authentifie le demandeur. L’authentificateur est également appelé serveur EAP.</td>
</tr>
<tr class="odd">
<td>Quelle est la durée de vie d’une authentification ?</td>
<td>La durée de vie d’une session d’authentification unique côté client correspond à tout ce qui se produit entre les fonctions [<strong>EapHostPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) et [<strong>EapHostPeerEndSession</strong>] (/Previous-versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) qui sont appelées. La durée de vie du côté de l’authentificateur est tout ce qui se produit entre les fonctions [<strong>EapPeerBeginSession</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) et [<strong>EapPeerEndSession</strong>] (/Previous-versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</td>
</tr>
<tr class="even">
<td>Qu’est-ce qu’un objet BLOB ? Pourquoi convertir un objet BLOB de configuration (binaire) en XML ?</td>
<td>Un objet BLOB est un objet binaire volumineux. XML présente plusieurs avantages par rapport à un objet BLOB de configuration binaire. Les données de configuration stockées dans XML sont explicites, modifiables et interplateformes.</td>
</tr>
<tr class="odd">
<td>Quand dois-je convertir un objet BLOB XML stocké en objet BLOB binaire ?</td>
<td>Il est possible de stocker un objet blob binaire ou un objet BLOB XML, mais vous devez toujours convertir l’objet BLOB XML en objet BLOB binaire avant de l’utiliser avec les API Runtime. les API Runtime ne peuvent pas accepter un répertoire XML.</td>
</tr>
<tr class="even">
<td>Que sont les méthodes natives ?</td>
<td>Les méthodes EAP natives utilisent la nouvelle API EAPHost.</td>
</tr>
<tr class="odd">
<td>Que sont les méthodes héritées ?</td>
<td>Les méthodes EAP héritées sont définies dans la référence du protocole EAP ( [Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)). Les méthodes EAP héritées sont disponibles pour une utilisation dans Windows Vista et Windows Server 2008. Ces méthodes peuvent ne pas être disponibles pour une utilisation dans les versions ultérieures du système d’exploitation.</td>
</tr>
<tr class="even">
<td>Quelle est la différence entre les méthodes héritées et natives ?</td>
<td>Les API natives sont plus simples et ont moins de fonctionnalités. Toutes les nouvelles méthodes EAP doivent être écrites à l’aide de l’API EAPHost.</td>
</tr>
<tr class="odd">
<td>Qu’est-ce que la &quot; stratégie de groupe &quot; ?</td>
<td>Pour obtenir une description de la stratégie de groupe, consultez [stratégie de groupe collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Les fonctions EAPHost peuvent-elles remplacer la stratégie de configuration spécifiée par la stratégie de groupe ?</td>
<td>Non, jamais. Si la stratégie de groupe est en cours d’utilisation, les paramètres de stratégie de groupe remplacent toujours les paramètres de configuration EAPHost.</td>
</tr>
<tr class="odd">
<td>Qu’est-ce que l’authentification unique (SSO) ?</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) est un mécanisme d’authentification de couche 2. Selon la configuration de l’authentification unique, l’authentification unique permet aux utilisateurs de s’authentifier sur le réseau à l’aide de l’authentification [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) avant ou immédiatement après l’ouverture de session sur Windows. L’authentification unique peut être configurée pour utiliser les informations d’identification Windows pour l’authentification réseau (dans ce cas, les utilisateurs entrent leurs informations d’identification une seule fois) ou utilisent des informations d’identification différentes pour l’authentification Windows et le réseau. Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).<br/></td>
</tr>
<tr class="even">
<td>Qu’est-ce que le fournisseur d’accès avant ouverture de session (PLAP)</td>
<td>Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).</td>
</tr>
<tr class="odd">
<td>Qu’est-ce que le protocole PEAP (Protected Extensible Authentication Protocol) ?</td>
<td>Pour plus d’informations, consultez [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) et [à propos du protocole EAP (Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol)).</td>
</tr>
<tr class="even">
<td>Comment PEAP gère-t-il la reprise de session et la ré-authentification ?</td>
<td>La réinitialisation et la réauthentification de la session se produisent généralement lors de l’itinérance sur un réseau sans fil. L’API de protection des données (DPAPI) Windows fournit un moyen de protéger et de lier des données à un utilisateur et éventuellement à la session de connexion. L’appelant donne à [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) une mémoire tampon non chiffrée et DPAPI chiffre la mémoire en place. Plus tard, l’appelant peut passer la mémoire tampon chiffrée à [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) et DPAPI déchiffrera la mémoire, une nouvelle fois en place. Pour plus d’informations, voir [extension d’application interne TLS (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) et [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).<br/></td>
</tr>
<tr class="odd">
<td>Qu’est-ce que la sécurité de niveau EAP-Transport (EAP-TLS) ?</td>
<td>EAP-TLS est un protocole client-serveur dans lequel des profils de certificat distincts sont généralement utilisés pour le client et le serveur. Pour plus d’informations, consultez [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/></td>
</tr>
<tr class="even">
<td>Comment faire implémenter une modification de mot de passe à l’aide de l’API LSA (local Security Authority) ?</td>
<td>Utilisez la fonction [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) pour implémenter une modification de mot de passe.</td>
</tr>
<tr class="odd">
<td>Pourquoi voulez-vous activer le suivi dans EAPHost ?</td>
<td>Les journaux de suivi contiennent des informations de débogage (disponibles en anglais uniquement) qui peuvent aider les développeurs et les partenaires Microsoft à trouver les causes racines des problèmes rencontrés avec le processus d’authentification. Pour plus d’informations, consultez [activation du suivi](enabling-tracing.md).<br/></td>
</tr>
<tr class="even">
<td>Pourquoi est-ce que je rencontre le code d’erreur NTE_BAD_KEY_STATE (0x8009000BL) lorsque j’utilise l’API de [chiffrement](/windows/desktop/SecCrypto/cryptography-portal) pour se connecter à l’échange EAP-TLS ?</td>
<td>Dans Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) est défini en tant que &quot; clé non valide pour une utilisation dans l’état spécifié &quot; . Cette erreur est généralement retournée dans les scénarios suivants.
<ul>
<li>Lors d’une tentative d’exportation d’un objet BLOB de clé privée non exportable</li>
<li>En cas de tentative infructueuse de génération d’un handle de hachage de fonction Pseudo-aléatoire (PRF) à l’aide de [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/WinCrypt/NF-WinCrypt-CryptCreateHash)</li>
</ul>
Pour plus d’informations, consultez [terminer les messages dans le protocole TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</td>
</tr>
<tr class="odd">
<td>Qu’est-ce qu’une fonction Pseudo-aléatoire (PRF) ?</td>
<td>Fonction qui prend une clé, une étiquette et une valeur initiale comme entrée, puis produit une sortie de longueur arbitraire. Pour plus d’informations, consultez [terminer les messages dans le protocole TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).<br/></td>
</tr>
<tr class="even">
<td>Comment EAPHost est-il lié aux cartes réseau ?</td>
<td>EAPHost permet à plusieurs demandeurs de fonctionner simultanément, et chaque demandeur peut se lier à plusieurs cartes réseau. Les demandeurs EAPHost fournissent une liaison avec les couches réseau et pilotent le processus d’authentification. Les demandeurs contiennent une configuration d’authentification. Les demandeurs enregistrent également l’État et fournissent la sécurité de connexion suivante. Comme EAPHost n’est pas directement lié à un mécanisme réseau, l’extensibilité du demandeur est possible.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[FAQ du demandeur EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[FAQ sur les méthodes EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[FAQ sur le développement EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>


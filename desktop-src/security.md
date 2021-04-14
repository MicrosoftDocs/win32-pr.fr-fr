---
description: Développez des applications de bureau plus sécurisées à l’aide des API et des services Windows.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Sécurité et identité
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5b8fccc4039794fe76dabb34d88fa6d475a3b22a
ms.sourcegitcommit: 7f0c005e444c17f69b5ead403c43814f3bbe047a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2020
ms.locfileid: "104383388"
---
# <a name="security-and-identity"></a>Sécurité et identité

Développez des applications de bureau plus sécurisées à l’aide des API et des services Windows. Ces API offrent les éléments suivants :

- Authentification
- Autorisation
- Chiffrement
- Services d’annuaire, d’identité et d’accès
- Contrôle parental
- Gestion des droits

Cette section présente également les meilleures pratiques et d’autres articles sur la sécurité.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
| ----- | ----------- |
| [Interface d’analyse anti-programme malveillant](./amsi/antimalware-scan-interface-portal.md) | L’interface d’analyse anti-programme malveillant (AMSI) est une norme d’interface générique qui permet aux applications et aux services de s’intégrer à n’importe quel produit logiciel anti-programme malveillant présent sur un ordinateur. Il offre une protection améliorée contre les programmes malveillants pour les utilisateurs et leurs données, applications et charges de travail. |
| [Authentification](./secauthn/authentication-portal.md) | L’authentification est le processus par lequel le système valide les informations d’ouverture de session d’un utilisateur. Le nom et le mot de passe d’un utilisateur sont comparés à une liste autorisée, et si le système détecte une correspondance, l’accès est accordé à l’étendue spécifiée dans la liste d’autorisations de cet utilisateur. |
| [Autorisation](./secauthz/authorization-portal.md) | L’autorisation est le droit accordé à un individu d’utiliser le système et les données qui y sont stockées. L’autorisation est généralement configurée par un administrateur système et vérifiée par l’ordinateur en fonction d’une forme d’identification utilisateur, telle qu’un numéro de code ou un mot de passe. |
| [Meilleures pratiques pour les API de sécurité](./secbp/best-practices-for-the-security-apis.md) | Fournit les meilleures pratiques pour le développement d’applications plus sûres. |
| [API d’inscription de certificats](./seccertenroll/certenroll-portal.md) | L’API d’inscription de certificats peut être utilisée pour créer une application cliente afin de demander un certificat et d’installer une réponse de certificat. |
| [Control Flow Guard (CFG) ](./secbp/control-flow-guard.md) | La protection de workflow de contrôle (CFG) est une fonctionnalité de sécurité de plateforme hautement optimisée qui a été créée pour combattre les vulnérabilités d’altération de la mémoire. |
| [Cryptographie](./seccrypto/cryptography-portal.md) | Le chiffrement consiste à utiliser des codes pour convertir des données afin que seul un destinataire spécifique puisse les lire à l’aide d’une clé. CryptoAPI permet aux utilisateurs de créer et d’échanger des documents et d’autres données dans un environnement sécurisé, en particulier sur des supports non sécurisés tels qu’Internet. |
| [API de chiffrement : nouvelle génération](./seccng/cng-portal.md) | Cryptography API : Next Generation (CNG) permet aux utilisateurs de créer et d’échanger des documents et d’autres données dans un environnement sécurisé, en particulier sur des supports non sécurisés tels qu’Internet. |
| [Extensibilité du développeur de Access Control dynamique](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | Le scénario de Access Control dynamique (DAC), tel qu’il est fourni dans Windows Server 2012, possède un large éventail de points d’extensibilité de développement qui ajoutent un potentiel de personnalisation pour le développement de vos applications. |
| [Services d’annuaire, d’identité et d’accès](./srvnodes/directory--identity--and-access-services.md) | Les administrateurs réseau peuvent utiliser les services d’annuaire pour automatiser les tâches administratives courantes, telles que l’ajout d’utilisateurs et de groupes, la gestion des imprimantes et la définition d’autorisations sur les ressources réseau.<br/> Les éditeurs de logiciels indépendants et les développeurs d’utilisateurs finaux peuvent utiliser des services d’annuaire pour activer l’annuaire de leurs produits et applications. Les services peuvent se publier eux-mêmes dans un répertoire, les clients peuvent utiliser l’annuaire pour rechercher des services, et les deux peuvent utiliser le répertoire pour rechercher et manipuler d’autres objets.<br/> Forefront Identity Manager (FIM) fournit une solution intégrée et complète pour gérer l’intégralité du cycle de vie des identités des utilisateurs et leurs informations d’identification associées.<br/> Identity Lifecycle Manager (ILM) permet aux organisations informatiques de réduire le coût de gestion du cycle de vie des identités et des accès en fournissant une vue unique de l’identité d’un utilisateur au sein de l’entreprise hétérogène et de l’automatisation des tâches courantes.<br/> Active Directory service FS (Federation Service) (AD FS) permet la gestion fédérée des identités et des accès en partageant en toute sécurité des droits d’identité et de droits numériques sur la sécurité et les limites de l’entreprise. |
| [Protocole EAP (Extensible Authentication Protocol)](./eap/extensible-authentication-protocol-reference.md) | Le protocole EAP (Extensible Authentication Protocol) est un standard pris en charge par plusieurs composants système. EAP est essentiel pour la protection de la sécurité des réseaux locaux sans fil (802.1 X) et des réseaux locaux câblés, des accès à distance et des réseaux privés virtuels (VPN). |
| [Hôte de protocole EAP (Extensible Authentication Protocol)](./eaphost/about-eap-host.md) | EAPHost est un composant de mise en réseau Microsoft Windows qui fournit une infrastructure EAP (Extensible Authentication Protocol) pour l’authentification des implémentations de protocole « demandeur », telles que 802.1 X et PPP (point-to-point). |
| [API de gestion des mots de passe MS-CHAP](/previous-versions/windows/desktop/mschap/portal) | Vous pouvez utiliser l’API de gestion des mots de passe MS-CHAP pour créer des applications afin de modifier les mots de passe des utilisateurs en réseau sur les stations de travail distantes. |
| [Protection d’accès réseau](./nap/network-access-protection-start-page.md) | La protection d’accès réseau (NAP) est un ensemble de composants du système d’exploitation qui fournissent une plateforme pour l’accès protégé aux réseaux privés. La plateforme NAP offre un moyen intégré d’évaluer l’état d’intégrité du système d’un client réseau qui tente de se connecter ou de communiquer sur un réseau et de restreindre l’accès du client réseau jusqu’à ce que les conditions de la stratégie de contrôle d’intégrité soient remplies. |
| [Serveur de stratégie réseau](./nps/portal.md) | Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS (Remote Authentication Dial-in User Service). Il s’agit du successeur du service d’authentification Internet (IAS). |
| [Contrôle parental](./parcon/parental-controls-portal.md) | La technologie de contrôle parental de Windows est destinée à aider les parents ou les gardiens de la diligence à garantir l’accès aux documents appropriés par âge ou par maturité pour ceux qui se trouvent dans leur tutelle. Il fournit une infrastructure extensible en plus des fonctionnalités intégrées. |
| [Rights Management](./srvnodes/rights-management.md) | Trois générations de Rights Management Kit de développement logiciel (SDK) sont désormais disponibles, ainsi qu’une feuille de route tout-en-un pour les outils de développement et les exemples de code RMS fournis par Microsoft sur tous les systèmes d’exploitation pris en charge. Android, iOS/OS X, Windows Phone et Windows Desktop. |
| [Cycle de vie de développement de la sécurité (SDL)-Guide de processus](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) est un processus de garantie de sécurité logiciel de pointe. Une initiative à l’ensemble de Microsoft et une stratégie obligatoire depuis 2004, le SDL a joué un rôle essentiel dans l’incorporation de la sécurité et de la confidentialité dans les logiciels et la culture Microsoft. Combinant une approche holistique et pratique, SDL introduit la sécurité et la confidentialité le plus tôt possible et dans toutes les phases du processus de développement. |
| [Gestion de la sécurité](./secmgmt/management-portal.md) | Les technologies de gestion de la sécurité peuvent être utilisées pour gérer la stratégie LSA (autorité de sécurité locale) et la stratégie de filtre de mot de passe, interroger la capacité des programmes à partir de sources externes et pièces jointes qui étendent les fonctionnalités de l’outil de configuration de la sécurité. |
| [Fournisseurs WMI de sécurité](./secprov/secprov-portal.md) | Les fournisseurs WMI de sécurité permettent aux administrateurs et aux programmeurs de configurer Chiffrement de lecteur BitLocker (BDE) et le Module de plateforme sécurisée (TPM) (TPM) à l’aide d’Windows Management Instrumentation (WMI). |
| [Glossaire sur la sécurité](./secgloss/security-glossary.md) | Fournit un glossaire des termes de sécurité. |
| [Services de base du module de plateforme sécurisée](./tbs/tpm-base-services-portal.md) | La fonctionnalité des services de base de la Module de plateforme sécurisée (TPM) (TBS) centralise l’accès au module de plateforme sécurisée entre les applications. La fonctionnalité TBS utilise des priorités spécifiées en appelant des applications pour planifier de manière coopérative l’accès au TPM. |
| [API WBF (Windows Biometric Framework)](./secbiomet/biometric-service-api-portal.md) | Vous pouvez utiliser l’API Windows Biometric Framework pour créer des applications clientes qui capturent, enregistrent et comparent en toute sécurité les informations biométriques de l’utilisateur final. |
| [Articles techniques sur la sécurité](https://msdn.microsoft.com/library/hh322936.aspx) | Articles sur la sécurité et le chiffrement. |



 

 

 
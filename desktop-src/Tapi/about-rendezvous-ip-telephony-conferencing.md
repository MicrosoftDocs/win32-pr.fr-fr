---
description: Les contrôles Rendezvous TAPI 3 fournissent des mécanismes permettant de publier et de découvrir des conférences IP multimédias multiparties. Les éléments suivants décrivent un ensemble de composants COM (Component Object Model) et d’interfaces permettant d’implémenter des conférences.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: À propos de la Conférence de téléphonie IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225f7842e0f7efdb97dcadc3d59adc8fa7e5adf0f73cd824b335500a5aa6c11d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949280"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a>À propos de la Conférence de téléphonie IP Rendezvous

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les contrôles Rendezvous TAPI 3 fournissent des mécanismes permettant de publier et de découvrir des conférences IP multimédias multiparties. Les éléments suivants décrivent un ensemble de composants COM (Component Object Model) et d’interfaces permettant d’implémenter des conférences.

COM est le modèle de codage de base pour TAPI 3, et vous savez qu’il est supposé dans ce document. Pour plus d’informations sur COM, consultez le kit de développement logiciel (SDK) de la plateforme.

## <a name="features"></a>Fonctionnalités

-   Fournit l’abstraction d’un répertoire de conférence pour manipuler les annonces de conférences multimédias.
-   Assure la sécurité par le biais de l’authentification, du chiffrement et d’une couche de contrôle d’accès (ACL) par annonce
-   Fournit un schéma commun pour une annonce de conférence, ce qui permet de rechercher des valeurs d’attribut
-   Autorise les extensions via un attribut géré par le fournisseur (objet blob de conférence) dans le schéma
-   Fournit un wrapper COM pour l’API d’allocation d’adresses multidiffusion (MADCAP)

## <a name="architecture"></a>Architecture

Les descriptions et le diagramme suivants illustrent les aspects clés de l’architecture système.

-   Le client peut manipuler des conférences stockées sur un répertoire dynamique ILS ou un serveur NTDS à l’aide des contrôles Rendezvous. Le protocole LDAP (Lightweight Directory Access Protocol) est utilisé pour communiquer avec un serveur ILS.
-   Les contrôles Rendezvous fournissent des interfaces COM doubles pour l’écriture de scripts et la programmation.
-   Un serveur SAP (session Announcement Protocol) ayant un accès direct à Internet écoute les annonces de conférences sur Internet et remplit les serveurs dynamiques ILS avec les informations de conférence. De même, il annonce également les conférences créées localement dont l’étendue comprend Internet. (le serveur SAP n’est pas planifié pour Microsoft Windows 2000.)

![architecture du système Rendezvous](images/rend1.png)

 

 




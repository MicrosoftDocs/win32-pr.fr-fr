---
title: Extensions du serveur NPS (Network Policy Server)
description: L’API extensions NPS permet aux développeurs de logiciels d’écrire des dll d’extension qui peuvent être utilisées pour l’authentification, l’autorisation et la gestion des comptes. L’API extensions NPS prend en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8db32889f266861809a0637dd380eb9f5d2ba7265bdf16d6a9404ed96a5420a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128769"
---
# <a name="network-policy-server-extensions"></a>Extensions du serveur NPS (Network Policy Server)

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

L’API extensions NPS permet aux développeurs de logiciels d’écrire des dll d’extension qui peuvent être utilisées pour l’authentification, l’autorisation et la gestion des comptes. L’API extensions NPS prend en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).

Les dll d’extension implémentées à l’aide de l’API d’extensions NPS peuvent fournir un contrôle et une gestion de session améliorés. Ces dll peuvent être utilisées dans des scénarios tels que le contrôle du nombre de sessions réseau de l’utilisateur final, l’utilisation d’un serveur d’État et la connexion aux bases de données d’authentification de domaine et aux services de Active Directory. Les dll d’extension peuvent étendre les autorisations d’accès à distance fournies par NPS en ajoutant leurs propres autorisations lors de l’envoi d’une réponse d’acceptation à un client d’authentification.

L’API extensions NPS s’applique dans tout environnement informatique où elle améliore l’efficacité pour authentifier les utilisateurs distants via un serveur distant. Cette technologie est particulièrement utile pour les fournisseurs de services Internet (ISP).

## <a name="in-this-section"></a>Dans cette section

[Vue d'ensemble](/windows/desktop/Nps/ias-about-internet-authentication-service)

Informations générales sur RADIUS et l’API des extensions NPS.

[À](/windows/desktop/Nps/ias-using-internet-authentication-service)

Exemple de code illustrant l’utilisation de l’API d’extensions NPS.

[Référence](/windows/desktop/Nps/ias-internet-authentication-service-reference)

Documentation des types, fonctions et structures énumérés qui composent l’API des extensions NPS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Serveur de stratégie réseau (service d’authentification Internet)](portal.md)
</dt> <dt>

[Protocole EAP (Extensible Authentication Protocol)](../eap/eap-start-page.md)
</dt> </dl>

 

 
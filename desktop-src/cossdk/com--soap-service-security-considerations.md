---
description: Considérations sur la sécurité du service SOAP COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Considérations sur la sécurité du service SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228275"
---
# <a name="com-soap-service-security-considerations"></a>Considérations sur la sécurité du service SOAP COM+

Le service SOAP COM+ dépend du serveur Web IIS pour la sécurité. Même en [mode d’objet activé](accessing-xml-web-services-in-cao-mode.md)par le client, un RPC com+ ne transmet pas l’identité du client et ne peut donc pas utiliser la sécurité basée sur les rôles ou toute autre fonctionnalité de sécurité fournie par DCOM. Si vous souhaitez protéger la confidentialité des données transmises vers et depuis votre service Web XML, ou pour protéger votre service Web XML contre tout accès non autorisé, vous pouvez configurer IIS pour limiter l’accès à un service Web XML en fonction de l’adresse IP des clients ou pour exiger qu’un client présente un certificat numérique pour vérifier son identité. Si vous ne limitez pas l’accès, tout client qui peut communiquer avec votre serveur Web peut accéder à votre service Web XML.

Vous pouvez configurer IIS pour chiffrer vos communications de service Web XML avec les clients à l’aide des protocoles SSL ou TLS de chiffrement à clé publique. Si vous ne chiffrez pas les communications SOAP, les données échangées entre un client et le serveur peuvent être observées par un tiers ayant accès à n’importe quel réseau sur lequel la communication SOAP transite ; en fonction de la topologie du réseau, il peut s’agir d’un petit réseau local ou d’Internet.

Par défaut, les communications SOAP non chiffrées sont reçues au niveau du port HTTP (80) et les communications SOAP chiffrées sont reçues au niveau du port HTTPs (443). Pour qu’un client accède correctement à un service Web XML, tous les pare-feu entre le client et le serveur doivent être configurés pour autoriser les paquets SYN TCP à atteindre le port serveur approprié. À l’inverse, pour limiter l’accès aux services Web XML, un administrateur de pare-feu peut choisir de fermer ces ports.

les paramètres de sécurité par défaut d’un composant COM exposé en tant que service web XML varient en fonction de la version de Microsoft .NET Framework installée. Si la version 1,0 est installée, les services Web XML ne sont pas sécurisés par défaut. tous les appels sont acceptés et aucun chiffrement n’est utilisé. Si la version 1,1 ou une version ultérieure est installée, les services Web XML sont sécurisés par défaut. les appelants doivent être authentifiés et le chiffrement est requis.

Un service Web XML sécurisé ne prend pas en charge l’accès WKO via WSDL. au lieu de cela, les clients qui ont installé la version de .NET Framework 1,1 peuvent l’appeler en mode CAO. Si des clients tiers ont besoin d’accéder à votre service Web XML via WSDL, vous devez autoriser l’accès anonyme.

Un composant COM exposé en tant que service Web XML s’exécute par défaut avec les autorisations de l’utilisateur anonyme (et non avec les autorisations de son appelant). Vous pouvez configurer IIS pour exécuter le service Web XML en tant qu’autre utilisateur ; Cela peut parfois être nécessaire, car votre composant utilise des fichiers ou d’autres ressources auxquels l’utilisateur anonyme n’a pas accès. Néanmoins, vous devez toujours essayer d’exécuter votre composant avec le moins de privilèges possible, afin de limiter les dommages qu’un appelant malveillant peut causer.

> [!Note]  
> Comme une méthode que vous avez exposée par le biais d’un service Web XML peut potentiellement être exposée à des appelants malveillants, vous devez toujours veiller à valider les paramètres d’entrée dont elle dépend.

 

Pour obtenir des instructions détaillées sur la configuration des paramètres de sécurité d’un service Web XML, consultez [sécurisation des services Web XML](securing-xml-web-services.md).

**Pour convertir une application SOAP sécurisée en application SOAP non sécurisée**

1.  ouvrez l’outil d’administration Internet Information Services (IIS).
2.  Recherchez le répertoire virtuel de l’application et ouvrez la boîte de dialogue **Propriétés** .
3.  Cochez la case **activer la page de contenu par défaut** sous l’onglet **documents** .
4.  Dans l’onglet **sécurité de répertoire** , cliquez sur **modifier** sous **accès anonyme et contrôle d’authentification**.
5.  Cochez la case **accès anonyme** pour activer l’accès anonyme, puis cliquez sur **OK**.
6.  Cliquez sur **modifier** sous **communications sécurisées**.
7.  Désactivez la case à cocher **exiger un canal sécurisé (SSL)** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> </dl>

 

 




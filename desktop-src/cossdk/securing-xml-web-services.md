---
description: L’accès aux applications COM+ exposées en tant que services Web XML est contrôlé par le serveur Web IIS, qui traite les demandes entrantes.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Sécurisation des services Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546962"
---
# <a name="securing-xml-web-services"></a>Sécurisation des services Web XML

L’accès aux applications COM+ exposées en tant que services Web XML est contrôlé par le serveur Web IIS, qui traite les demandes entrantes. Vous pouvez également configurer IIS pour exiger que les communications avec l’appelant s’effectuent sur un canal sécurisé établi à l’aide du protocole SSL (Secure Sockets Layer) (SSL).

> [!Note]  
> Un service Web XML sécurisé ne prend pas en charge l’accès WKO via WSDL. au lieu de cela, les clients qui ont installé la version de .NET Framework 1,1 peuvent l’appeler en mode CAO. Si des clients tiers ont besoin d’accéder à votre service Web XML via WSDL, vous devez autoriser l’accès anonyme.

 

> [!Note]  
> Pour utiliser le protocole SSL afin d’établir un canal de communication sécurisé, vous devez obtenir et installer un certificat SSL.

 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour sélectionner le mécanisme d’authentification d’un service Web XML, procédez comme suit :

1.  Cliquez avec le bouton droit sur l’icône de **poste de travail** sur votre bureau, puis cliquez sur **gérer**.

2.  Sous **services et applications** et **Internet Information Services**, recherchez l’icône correspondant au répertoire racine virtuel de votre service Web XML. Cliquez avec le bouton droit sur l’icône du répertoire, puis choisissez **Propriétés**.

3.  Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, recherchez **authentification et contrôle d’accès** , puis cliquez sur le bouton **modifier** correspondant.

4.  Dans la boîte de dialogue **méthodes d’authentification** , sous **accès authentifié**, utilisez les cases à cocher pour sélectionner les mécanismes d’authentification que vous souhaitez autoriser. Cliquez sur **OK**.

    > [!Note]  
    > vous pouvez configurer iis pour authentifier les appelants en utilisant l’une des options suivantes dans la boîte de dialogue **méthodes d’authentification** iis : **authentification Windows intégrée**, **authentification Digest pour les serveurs de domaine Windows**, **authentification de base (mot de passe envoyé en texte clair)** ou **authentification .net Passport**. Vous pouvez également autoriser l’accès anonyme.

     

5.  Dans la boîte de dialogue Propriétés, cliquez sur **OK**.

Pour autoriser un accès anonyme non sécurisé à un service Web XML, procédez comme suit :

1.  Cliquez avec le bouton droit sur l’icône de **poste de travail** sur votre bureau, puis cliquez sur **gérer**.

2.  Sous **services et applications** et **Internet Information Services**, recherchez l’icône correspondant au répertoire racine virtuel de votre service Web XML. Cliquez avec le bouton droit sur l’icône du répertoire, puis choisissez **Propriétés**.

3.  Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, recherchez **authentification et contrôle d’accès**, puis cliquez sur le bouton **modifier** correspondant. Activez la case à cocher **activer la connexion anonyme** . Cliquez sur **OK**.

4.  Sous l’onglet **sécurité de répertoire** de la boîte de dialogue Propriétés, localisez **communications sécurisées** , puis cliquez sur le bouton **modifier** correspondant. Désactivez la case à cocher **exiger un canal sécurisé (SSL)** . Cliquez sur **OK**.

5.  Dans la boîte de dialogue Propriétés, cliquez sur **OK**.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Non applicable.

## <a name="additional-security-considerations"></a>Considérations supplémentaires sur la sécurité

En exigeant un canal sécurisé, vous contribuez à protéger la confidentialité des données échangées en chiffrant les communications entre le client et votre service Web XML. Si vous autorisez l’authentification à l’aide de mots de passe en texte clair, vous devez exiger un canal sécurisé afin d’éviter d’exposer les mots de passe sur le réseau.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accès aux services Web XML en mode WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Considérations sur la sécurité du service SOAP COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Création de services Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 




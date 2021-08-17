---
description: L’autorisation définit les ressources auxquelles vous avez accès.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorisation pour les pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141325"
---
# <a name="authorization-for-web-pages"></a>Autorisation pour les pages Web

L’autorisation définit les ressources auxquelles vous avez accès.

**Objectif :** Pour permettre aux utilisateurs d’accéder à votre application.

## <a name="prerequisites"></a>Prérequis

Aucun

**Durée :** 2 minutes.

## <a name="instructions"></a>Instructions

### <a name="1-authorization"></a>1. autorisation

Lorsque l’utilisateur entre ses informations d’identification et clique sur le bouton de connexion, la page autorisations s’affiche. Cette page est idéale pour permettre aux utilisateurs de contrôler des autorisations granulaires afin d’accorder à l’application l’accès aux données de contoso. ![page autorisations contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. utilisation de l’exemple

Vous devez connaître les fichiers HTML et CSS suivants.

1.  Les fichiers HTML suivants correspondent aux deux pages du workflow d’autorisation Web
    -   WebAuthLogin.html – exemple de code HTML pour la page de connexion
    -   WebAuthPermissions.html – exemple de code HTML pour la page autorisations
2.  les fichiers CSS contiennent Windows 8 styles pour faciliter la création d’une page web d’application Windows Store.
    -   ui-light. css : cela a été dérivé de la feuille de style de base pour les contrôles Windows 8.
    -   UI-webauth. CSS : fournit un style incrémentiel pour optimiser la disposition des pages d’authentification Web.
    -   Theme-Colors. CSS : fournit le style incrémentiel pour remplacer les couleurs d’accentuation par défaut des contrôles par la couleur de la personnalisation du fournisseur.

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

[Didacticiel Résumé pour l’authentification des pages Web](tutorial-for-authenticating-web-pages.md)

[Meilleures pratiques pour concevoir des pages Web d’authentification](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur le développement de pages web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

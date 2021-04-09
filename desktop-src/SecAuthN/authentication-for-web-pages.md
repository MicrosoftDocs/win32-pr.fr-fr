---
description: L’authentification est la preuve de votre identité.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Authentification pour les pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952638"
---
# <a name="authentication-for-web-pages"></a>Authentification pour les pages Web

L’authentification est la preuve de votre identité.

**Objectif :** Pour que le Service Broker d’authentification Web apparaisse dans le cadre de votre application.

## <a name="prerequisites"></a>Prérequis

Aucun

**Durée d’exécution :** 15 minutes.

## <a name="instructions"></a>Instructions

### <a name="1-getting-started"></a>1. Mise en route

Lancez le fichier d’installation pour installer un site Web Contoso dans Internet Information Services 8 sur l’ordinateur local afin d’héberger les fichiers HTML et CSS de l’exemple.

1.  Des exemples de fichiers HTML et CSS seront installés dans le répertoire Program Files de Microsoft \\ contoso.
2.  En outre, une application du Windows Store « Fabrikam social » sera déconditionnée sur le bureau.

### <a name="2-getting-familiar"></a>2. Familiarisez-vous avec

Pour avoir une idée de ce à quoi ressemblent les exemples de pages dans le répartiteur d’authentification Web, ouvrez le fichier solution Fabrikam de Visual Studio 11 social dans le dossier « Fabrikam social » sur le bureau.

1.  Exécutez l’application et appuyez sur « Démarrer » pour afficher les exemples de pages dans le répartiteur d’authentification Web.
2.  L’application peut être redimensionnée d’un côté ou activée en partageant des données à l’application.

### <a name="3-authentication"></a>3. Authentification

Lorsque l’API d’authentification Web est appelée par l’application sous-jacente pour se connecter au fournisseur, « contoso social », la page de connexion s’affiche. Cette page est conçue pour offrir une expérience de connexion rapide et fluide. Il fournit également des points d’entrée pour d’autres actions courantes de l’utilisateur, telles que la récupération des informations de mot de passe, l’inscription à un compte et la lecture d’instructions sur la confidentialité et les conditions générales qui sont terminées dans le navigateur. ![page de connexion contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Résumé et étapes suivantes

[Didacticiel Résumé pour l’authentification des pages Web](tutorial-for-authenticating-web-pages.md)

[Autorisation suivante pour les pages Web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur le développement de pages web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

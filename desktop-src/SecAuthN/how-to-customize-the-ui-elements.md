---
description: Une page Web personnalise l’interface utilisateur avec le titre, l’icône et la couleur d’en-tête à l’aide des balises de métadonnées définies sur la page Web.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Guide pratique pour personnaliser les éléments de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a99e8e7da789653226db40763116472eb065df0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884558"
---
# <a name="how-to-customize-the-ui-elements"></a>Guide pratique pour personnaliser les éléments de l’interface utilisateur

Une page Web personnalise l’interface utilisateur avec le titre, l’icône et la couleur d’en-tête à l’aide des balises de métadonnées définies sur la page Web. Les développeurs Web peuvent utiliser &lt; des &gt; balises méta html pour afficher la personnalité et la marque du fournisseur dans l’interface utilisateur du répartiteur d’authentification Web. En outre, les développeurs peuvent diriger des actions utilisateur plus complexes, par exemple l’inscription et la récupération des mots de passe. le concept est très similaire à la fonctionnalité de Sites épinglés de la Windows Internet Explorer 9 et Windows 7.

outre la personnalisation de l’interface utilisateur autour de la zone de page web, la page web doit également tirer parti des styles du Windows 8 contrôles, être activée pour la saisie tactile et permettre l’ouverture des liens dans le navigateur, le cas échéant.

Voici un exemple de page Web qui a tiré parti du modèle de personnalisation du Service Broker d’authentification Web. ![éléments de l’interface utilisateur du répartiteur d’authentification Web](images/wab-figure7.png)

## <a name="instructions"></a>Instructions

### <a name="step-1-customize-the-icon"></a>Étape 1 : personnaliser l’icône

La page Web peut fournir une icône à l’aide d’une balise méta mswebdialog.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

Le contenu est une URL qui peut être une page relative ou absolue. Le schéma de l’URL peut être HTTP ou HTTPs. Le format du fichier doit être PNG ou JPG. La taille de l’image doit être de 30x30 pixels. Si l’image est de la taille différente, elle est mise à l’échelle vers le haut ou vers le haut par le système d’exploitation pour correspondre à l’espace 30x30. L’image doit être conçue pour s’afficher correctement lorsqu’elle est mise à l’échelle jusqu’à 140% et 180% pour prendre en compte les écrans de résolution plus élevée. pour tester différents facteurs de mise à l’échelle, utilisez l' [exemple d’application du kit de développement logiciel (SDK) du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) chargé dans Visual Studio 11, qui permet de simuler différentes résolutions et facteurs de mise à l’échelle à l’aide des fenêtres d’appareil du mode création.

### <a name="step-2-customize-the-title-text"></a>Étape 2 : personnaliser le texte du titre

La page Web peut fournir le titre à l’aide de la balise Meta mswebdialog-title.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

Le titre doit être abrégé et doit refléter la personnalisation du fournisseur (par exemple, contoso).

### <a name="step-3-customize-the-header-color"></a>Étape 3 : personnaliser la couleur d’en-tête

La page Web peut fournir la couleur qui représente son identité de marque à utiliser pour l’en-tête de la boîte de dialogue à l’aide de la balise Meta mswebdialog-Header-Color.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

La couleur peut être n’importe quelle valeur spécifiée ici. Toutefois, le Service Broker d’authentification Web ignore toute valeur de canal alpha. avec cette couleur et les couleurs utilisées sur la page en général, il est recommandé de suivre les mêmes couleurs que celles utilisées dans l’application Windows 8 du fournisseur si cette application existe.

> [!Note]  
> Les icônes et les couleurs sont mises en cache par serveur sur le client une fois que les balises méta sont analysées. Effacez le cache du client avant de lancer l’interface utilisateur afin que les modifications soient prises en compte. Pour ce faire, modifiez les paramètres de registre suivants.

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

Une fois qu’une icône est téléchargée, elle n’est pas récupérée dans les 24 heures. Pour effectuer un test avec des images de logo, définissez la clé de Registre ci-dessus avec une valeur inférieure.

### <a name="step-4-customize-the-web-page"></a>Étape 4 : personnaliser la page Web

outre la personnalisation de l’interface utilisateur sur la page web, les développeurs doivent également créer des pages web qui sont transparents et intégrées avec l’expérience d’Windows 8 globale. Cela comprend l’utilisation de styles recommandés, en veillant à ce que les pages Web fonctionnent bien avec les appareils tactiles et ouvrent certaines pages Web dans le navigateur Web.

-   Style

    Il est vivement recommandé d’utiliser le style recommandé ici pour créer une expérience utilisateur plus cohérente entre les pages Web du Service Broker d’authentification Web et d’autres composants d’interface utilisateur de Windows 8. La page Web doit utiliser un arrière-plan blanc et aucune bordure. Les boutons tels que connexion ou annuler doivent être positionnés à l’angle inférieur droit et utiliser la même couleur que l’en-tête. Enfin, étant donné que le Service Broker d’authentification Web fournit un bouton précédent, envisagez d’éliminer complètement un bouton Annuler de la page Web.

-   Activation de Touch

    La page Web doit être conçue avec une interaction tactile de l’utilisateur à l’esprit. pour plus d’informations sur la conception pour la saisie tactile dans Windows 8, consultez la rubrique [conception d’interaction tactile](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) .

-   Personnalisation de la cible des liens hypertexte

    Le Service Broker d’authentification Web est idéal pour la diffusion de pages Web nécessitant une action d’utilisateur unique, par exemple, les pages de connexion ou d’autorisation OAuth. Toutefois, pour des flux d’utilisateurs plus complexes tels que la création de comptes, la récupération à partir d’un mot de passe perdu ou oublié, l’indication des déclarations de confidentialité, etc., où l’utilisateur doit investir du temps pour comprendre et terminer le flux, il est recommandé de lancer ces pages dans le navigateur préféré de l’utilisateur pour prendre en charge la navigation complète et la navigation. Par défaut, le Service Broker d’authentification Web n’autorise pas l’ouverture de nouvelles fenêtres de navigateur à partir d’une page Web (pour plus d’informations, consultez la section aucune nouvelle fenêtre par défaut). Toutefois, à l’aide de la balise Meta, `mswebdialog-newwindowurl` la page Web peut déclarer quelles URL doivent être ouvertes dans le navigateur.

    `mswebdialog-newwindowurl`Permet à la page Web de spécifier une URL ou une partie de l’URL qui sera utilisée par le répartiteur d’authentification Web pour la correspondance (correspondance de chaîne à gauche) par rapport à chaque fois qu’il est invité à ouvrir une URL dans une nouvelle fenêtre à l’aide de la méthode attribute target ou Window. Open (). En cas de correspondance, l’URL est ouverte dans le navigateur par défaut de l’utilisateur. Si aucune correspondance n’est trouvée, le répartiteur d’authentification Web accède à l’URL proprement dite (comportement par défaut). Par exemple :`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    Dans le cas de cette balise Meta, le répartiteur d’authentification Web ouvre le https://www.contoso.com/privacy/policy.html dans le navigateur, mais accède directement à https://www.contoso.com/termsofuse.html . Notez que les liens qui ne tentent pas de s’ouvrir dans une nouvelle fenêtre (par exemple, les liens qui n’utilisent pas l’attribut Target ou la méthode Window. Open ()) ne sont pas affectés par cette balise meta. Le contenu est une URL qui peut être une page relative ou absolue. Le schéma de l’URL peut être HTTP ou HTTPs. Vous devez définir des `mswebdialog-newwindowurl` balises méta pour couvrir tous les liens qui ne font pas partie du workflow d’utilisateur de base, tels que les déclarations de confidentialité, les formulaires d’inscription et ainsi de suite. Si vous prenez en charge la connexion avec un fournisseur d’authentification tiers (par exemple, les fournisseurs OpenID), veillez à conserver ces interactions dans le répartiteur d’authentification Web. Pour permettre l’ouverture de tous les liens de votre page en toute sécurité dans le navigateur, utilisez la syntaxe en étoile, telle que, `  <meta name="mswebdialog-newwindowurl" content="*"/>` Notez que le « \* » ne peut être utilisé qu’en exclusivité et ne peut pas être combiné avec une autre URL, par exemple, « https://www.contoso.com/\ * » n’est pas une syntaxe valide.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Étape 5 : règles appliquées à toutes les balises méta

Lorsque le Service Broker d’authentification Web traite les balises méta, les règles suivantes s’appliquent :

-   L’effet de la balise Meta est conservé dans toutes les pages sous le même domaine de deuxième niveau (par exemple, contoso.com), sauf si une autre balise Meta portant le même nom mais un contenu différent est rencontrée.
-   Si plusieurs balises méta du même nom sont rencontrées sur la même page, le répartiteur d’authentification Web ne choisit qu’un seul d’entre eux et ignore le reste. La balise Meta spécifique choisie n’est pas définie.
    > [!Note]  
    > Cette règle ne s’applique pas à la `mswebdialog-newwindowurl` balise méta qui autorise plusieurs instances sur la même page.

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur le développement de pages web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

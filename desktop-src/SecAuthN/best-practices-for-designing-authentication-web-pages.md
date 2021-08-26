---
description: Cette rubrique décrit les meilleures pratiques pour concevoir des pages Web qui utilisent le Service Broker d’authentification Web pour la connexion.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Bonnes pratiques pour concevoir des pages web d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80fbf38c0e020cad342331d67278818b56ce331ff39434aefd726dea52bae1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883611"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Bonnes pratiques pour concevoir des pages web d’authentification

Cette rubrique décrit les meilleures pratiques pour concevoir des pages Web qui utilisent le Service Broker d’authentification Web pour la connexion.

-   [Utilisation des métabalises](#use-of-metatags)
-   [utilisation de Windows 8 styles CSS](#use-of-windows-8-css-styling)
-   [Utilisation des couleurs et des thèmes](#use-of-color-and-themes)
-   [Alignment](#alignment)
-   [Conception pour l’alignement](#designing-for-snap)
-   [Conception pour une expérience de connexion rapide et fluide](#designing-for-a-fast-and-fluid-login-experience)
-   [Security Considerations](#security-considerations)
-   [Rubriques connexes](#related-topics)

## <a name="use-of-metatags"></a>Utilisation des métabalises

À l’aide des métabalises, le fournisseur « contoso social » peut spécifier le titre, l’icône et la couleur de l’en-tête. Dans l’exemple de fichier HTML (WebAuthLogin.html), cette opération s’effectue à l’aide du code suivant.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



cela permet à Windows d’intégrer la présence du fournisseur de manière bien visible dans l’en-tête de l’interface utilisateur, tel qu’il est mis en surbrillance par le cadre rouge dans la capture d’écran suivante. ![page de connexion avec l’en-tête Contoso dans l’interface utilisateur](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>utilisation de Windows 8 styles CSS

la feuille de style ui-light. css fournie est la feuille de style Windows 8 utilisée par les applications Windows store. il définit Windows style de l’application du Store pour la typographie et les contrôles standard, tels que les boutons, les zones de texte, les liens hypertexte et les cases à cocher pour s’assurer qu’ils sont conviviaux. lors de la conception et de l’adaptation des pages d’autorisation web pour Windows 8, nous vous encourageons à utiliser cette feuille de style telle quelle et à la mettre à jour en fonction des besoins tant que votre page web suit toujours les meilleures pratiques de manière autonome.

par exemple, si vous avez une feuille de style spéciale pour les liens hypertexte qui doivent ressembler à votre page web, il est judicieux de vous assurer que le style que vous fournissez est convivial de la même façon que les liens hypertexte standard Windows 8. cela est essentiel pour la base des consommateurs qui utilise Windows 8 sur leurs appareils tactiles.

## <a name="use-of-color-and-themes"></a>Utilisation des couleurs et des thèmes

Cet exemple illustre une utilisation réfléchie de la couleur de différentes façons.

-   Arrière-plan blanc pour la page Web. Comme vous pouvez le constater dans la capture d’écran précédente, la page Web est hébergée dans une surface blanche qui s’étend sur la largeur de l’écran. Pour vous assurer que la page Web s’intègre à la surface, il est recommandé que la page Web ait un arrière-plan blanc.
-   Coloriser les contrôles en fonction de la couleur de la personnalisation. Le fichier CSS Theme-Colors. CSS fournit un style permettant de substituer les couleurs standard des contrôles dans la feuille de style UI-Light pour les faire correspondre aux couleurs de l’en-tête. Par exemple, dans la capture d’écran suivante, les boutons et les liens hypertexte prennent les couleurs dérivées de la couleur d’en-tête. ![capture d’écran des boutons et du texte avec la même couleur que l’en-tête](images/wab-figure11.png)
-   Couleur d’en-tête. L’utilisation de la couleur de la personnalisation de Contoso dans l’en-tête crée une personnalité unifiée pour la personnalisation du fournisseur dans l’interface utilisateur du système.

## <a name="alignment"></a>Alignment

La page Web elle-même n’a pas de remplissage à gauche ou à droite pour permettre l’alignement typographique avec le titre dans l’en-tête sur la gauche et l’icône dans l’en-tête à droite.

Vous remarquerez également que les boutons sont toujours alignés en bas à droite dans la page Web (et alignés à droite avec l’icône dans l’en-tête). il s’agit de la meilleure pratique, car Windows 8 utilisateurs seront habitués aux flux de dialogue similaires avec des boutons en bas à droite.

## <a name="designing-for-snap"></a>Conception pour l’alignement

Dans l’image suivante, vous pouvez voir les pages de connexion et d’autorisation dans état du composant logiciel enfichable.

![vue d’alignement de l’écran de connexion ](images/wab-figure12.png) . ![vue d’alignement de la page autorisations ](images/wab-figure13.png)

Dans l’exemple de fichier UI-webauth. CSS, vous pouvez voir l’utilisation de requêtes de média qui optimisent la disposition de la page pour l’état de l’alignement en fonction de la largeur disponible pour la page Web. L’extrait de code inclus dans l’étendue suivante implémente CSS adapté à l’état d’alignement.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



dans Windows 8, la largeur de l’état du magnétisme est de 320 pixels. La page d’authentification Web occupe 260 pixels dans l’interface utilisateur ci-dessus. Nous utilisons une valeur de largeur maximale avec suffisamment de marge. par conséquent, le code de requête de média du fournisseur n’est pas lié à la largeur exacte de l’état d’alignement.

Pour adapter votre application à la vue d’alignement, il est important que l’utilisateur ne perde aucun contexte dans les autres modes d’authentification Web (affichages plein, remplissage ou icône), mais il est utile de restructurer la disposition et la hiérarchie des éléments de la page pour que les informations nécessaires à la conservation du contexte soient visibles et interactives. Nous avons fait appel à des exemples de la façon dont l’exemple personnalise la page Web pour l’état de l’alignement.

-   Par exemple, pour la page de connexion dans l’état de l’alignement, la propriété Width du champ de texte d’entrée (comme spécifié dans UI-Light. CSS) a été remplacée et définie comme une valeur numérique inférieure, afin que le champ de texte ne soit pas tronqué horizontalement.
-   Autre exemple : dans l’état d’alignement, la taille de police des en-têtes H1 et H2 est réduite à 20 PT et 11 PT de 42 PT et 20 PT respectivement. cette opération est effectuée conformément à la rampe de type Windows 8 et optimise le texte pour qu’il soit plus compact dans la fenêtre d’affichage modifiée.
-   En guise d’autre exemple, Notez que les tailles des icônes dans la page autorisations sont plus petites (comparer à la page vue complète ci-dessus). Là encore, cette opération est effectuée pour conserver le contexte, tout en échangeant les ressources de conception pour celles qui sont les plus optimales pour la fenêtre d’affichage modifiée.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Conception pour une expérience de connexion rapide et fluide

Au début de la conception de cette page Web, nous avons fait un intérêt dans le fait que cette page est la meilleure pour une expérience de connexion rapide et fluide. Par conséquent, l’interface utilisateur qui est la plus visible dans le Flow est le champ nom d’utilisateur et mot de passe de la page de connexion pour une expérience d’entrée d’informations d’identification rapide. Bien que nous ayons identifié qu’il existe d’autres scénarios courants tels que la récupération du mot de passe et le référencement des déclarations de confidentialité, la riche expérience du Web est un meilleur emplacement pour ces expériences. Pour tous les flux qui ne sont pas liés à l’authentification Web sécurisée, nous vous recommandons de naviguer dans le navigateur de l’utilisateur. Cela est illustré dans l’exemple de fichier HTML (WebAuthLogin.html) comme suit : `<meta name="mswebdialog-newwindowurl" content="*" />` ouvre toutes les pages Web liées à à partir de la page de connexion ou d’autorisations dans le navigateur par défaut de l’utilisateur où l’utilisateur peut effectuer ces flux, puis revenir à l’application pour se connecter.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Les articles suivants fournissent des conseils pour l’écriture de code C++ sécurisé.

-   [Meilleures pratiques de sécurité pour C++](/cpp/security/security-best-practices-for-cpp)
-   [Modèles & pratiques conseils de sécurité pour les applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur le développement de pages web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Forum aux questions sur le Service Broker d’authentification Web](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Exemple d’application du SDK du Broker d’authentification Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

---
description: Cette rubrique décrit les meilleures pratiques pour concevoir des pages Web qui utilisent le Service Broker d’authentification Web pour la connexion.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Bonnes pratiques pour concevoir des pages web d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353672"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="bc0e5-103">Bonnes pratiques pour concevoir des pages web d’authentification</span><span class="sxs-lookup"><span data-stu-id="bc0e5-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="bc0e5-104">Cette rubrique décrit les meilleures pratiques pour concevoir des pages Web qui utilisent le Service Broker d’authentification Web pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="bc0e5-105">Utilisation des métabalises</span><span class="sxs-lookup"><span data-stu-id="bc0e5-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="bc0e5-106">utilisation de Windows 8 styles CSS</span><span class="sxs-lookup"><span data-stu-id="bc0e5-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="bc0e5-107">Utilisation des couleurs et des thèmes</span><span class="sxs-lookup"><span data-stu-id="bc0e5-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="bc0e5-108">Alignment</span><span class="sxs-lookup"><span data-stu-id="bc0e5-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="bc0e5-109">Conception pour l’alignement</span><span class="sxs-lookup"><span data-stu-id="bc0e5-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="bc0e5-110">Conception pour une expérience de connexion rapide et fluide</span><span class="sxs-lookup"><span data-stu-id="bc0e5-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="bc0e5-111">Security Considerations</span><span class="sxs-lookup"><span data-stu-id="bc0e5-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="bc0e5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc0e5-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="bc0e5-113">Utilisation des métabalises</span><span class="sxs-lookup"><span data-stu-id="bc0e5-113">Use of metatags</span></span>

<span data-ttu-id="bc0e5-114">À l’aide des métabalises, le fournisseur « contoso social » peut spécifier le titre, l’icône et la couleur de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="bc0e5-115">Dans l’exemple de fichier HTML (WebAuthLogin.html), cette opération s’effectue à l’aide du code suivant.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="bc0e5-116">cela permet à Windows d’intégrer la présence du fournisseur de manière bien visible dans l’en-tête de l’interface utilisateur, tel qu’il est mis en surbrillance par le cadre rouge dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![page de connexion avec l’en-tête Contoso dans l’interface utilisateur](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="bc0e5-118">utilisation de Windows 8 styles CSS</span><span class="sxs-lookup"><span data-stu-id="bc0e5-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="bc0e5-119">la feuille de style ui-light. css fournie est la feuille de style Windows 8 utilisée par les applications Windows store.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="bc0e5-120">il définit Windows style de l’application du Store pour la typographie et les contrôles standard, tels que les boutons, les zones de texte, les liens hypertexte et les cases à cocher pour s’assurer qu’ils sont conviviaux.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="bc0e5-121">lors de la conception et de l’adaptation des pages d’autorisation web pour Windows 8, nous vous encourageons à utiliser cette feuille de style telle quelle et à la mettre à jour en fonction des besoins tant que votre page web suit toujours les meilleures pratiques de manière autonome.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="bc0e5-122">par exemple, si vous avez une feuille de style spéciale pour les liens hypertexte qui doivent ressembler à votre page web, il est judicieux de vous assurer que le style que vous fournissez est convivial de la même façon que les liens hypertexte standard Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="bc0e5-123">cela est essentiel pour la base des consommateurs qui utilise Windows 8 sur leurs appareils tactiles.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="bc0e5-124">Utilisation des couleurs et des thèmes</span><span class="sxs-lookup"><span data-stu-id="bc0e5-124">Use of color and themes</span></span>

<span data-ttu-id="bc0e5-125">Cet exemple illustre une utilisation réfléchie de la couleur de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="bc0e5-126">Arrière-plan blanc pour la page Web.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-126">White background for the web page.</span></span> <span data-ttu-id="bc0e5-127">Comme vous pouvez le constater dans la capture d’écran précédente, la page Web est hébergée dans une surface blanche qui s’étend sur la largeur de l’écran.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="bc0e5-128">Pour vous assurer que la page Web s’intègre à la surface, il est recommandé que la page Web ait un arrière-plan blanc.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="bc0e5-129">Coloriser les contrôles en fonction de la couleur de la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="bc0e5-130">Le fichier CSS Theme-Colors. CSS fournit un style permettant de substituer les couleurs standard des contrôles dans la feuille de style UI-Light pour les faire correspondre aux couleurs de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="bc0e5-131">Par exemple, dans la capture d’écran suivante, les boutons et les liens hypertexte prennent les couleurs dérivées de la couleur d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![capture d’écran des boutons et du texte avec la même couleur que l’en-tête](images/wab-figure11.png)
-   <span data-ttu-id="bc0e5-133">Couleur d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-133">Header color.</span></span> <span data-ttu-id="bc0e5-134">L’utilisation de la couleur de la personnalisation de Contoso dans l’en-tête crée une personnalité unifiée pour la personnalisation du fournisseur dans l’interface utilisateur du système.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="bc0e5-135">Alignment</span><span class="sxs-lookup"><span data-stu-id="bc0e5-135">Alignment</span></span>

<span data-ttu-id="bc0e5-136">La page Web elle-même n’a pas de remplissage à gauche ou à droite pour permettre l’alignement typographique avec le titre dans l’en-tête sur la gauche et l’icône dans l’en-tête à droite.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="bc0e5-137">Vous remarquerez également que les boutons sont toujours alignés en bas à droite dans la page Web (et alignés à droite avec l’icône dans l’en-tête).</span><span class="sxs-lookup"><span data-stu-id="bc0e5-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="bc0e5-138">il s’agit de la meilleure pratique, car Windows 8 utilisateurs seront habitués aux flux de dialogue similaires avec des boutons en bas à droite.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="bc0e5-139">Conception pour l’alignement</span><span class="sxs-lookup"><span data-stu-id="bc0e5-139">Designing for snap</span></span>

<span data-ttu-id="bc0e5-140">Dans l’image suivante, vous pouvez voir les pages de connexion et d’autorisation dans état du composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="bc0e5-141">vue d’alignement de l’écran de connexion</span><span class="sxs-lookup"><span data-stu-id="bc0e5-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="bc0e5-142">.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-142">.</span></span> ![<span data-ttu-id="bc0e5-143">vue d’alignement de la page autorisations</span><span class="sxs-lookup"><span data-stu-id="bc0e5-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="bc0e5-144">Dans l’exemple de fichier UI-webauth. CSS, vous pouvez voir l’utilisation de requêtes de média qui optimisent la disposition de la page pour l’état de l’alignement en fonction de la largeur disponible pour la page Web.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="bc0e5-145">L’extrait de code inclus dans l’étendue suivante implémente CSS adapté à l’état d’alignement.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="bc0e5-146">dans Windows 8, la largeur de l’état du magnétisme est de 320 pixels.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="bc0e5-147">La page d’authentification Web occupe 260 pixels dans l’interface utilisateur ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="bc0e5-148">Nous utilisons une valeur de largeur maximale avec suffisamment de marge. par conséquent, le code de requête de média du fournisseur n’est pas lié à la largeur exacte de l’état d’alignement.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="bc0e5-149">Pour adapter votre application à la vue d’alignement, il est important que l’utilisateur ne perde aucun contexte dans les autres modes d’authentification Web (affichages plein, remplissage ou icône), mais il est utile de restructurer la disposition et la hiérarchie des éléments de la page pour que les informations nécessaires à la conservation du contexte soient visibles et interactives.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="bc0e5-150">Nous avons fait appel à des exemples de la façon dont l’exemple personnalise la page Web pour l’état de l’alignement.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="bc0e5-151">Par exemple, pour la page de connexion dans l’état de l’alignement, la propriété Width du champ de texte d’entrée (comme spécifié dans UI-Light. CSS) a été remplacée et définie comme une valeur numérique inférieure, afin que le champ de texte ne soit pas tronqué horizontalement.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="bc0e5-152">Autre exemple : dans l’état d’alignement, la taille de police des en-têtes H1 et H2 est réduite à 20 PT et 11 PT de 42 PT et 20 PT respectivement.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="bc0e5-153">cette opération est effectuée conformément à la rampe de type Windows 8 et optimise le texte pour qu’il soit plus compact dans la fenêtre d’affichage modifiée.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="bc0e5-154">En guise d’autre exemple, Notez que les tailles des icônes dans la page autorisations sont plus petites (comparer à la page vue complète ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="bc0e5-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="bc0e5-155">Là encore, cette opération est effectuée pour conserver le contexte, tout en échangeant les ressources de conception pour celles qui sont les plus optimales pour la fenêtre d’affichage modifiée.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="bc0e5-156">Conception pour une expérience de connexion rapide et fluide</span><span class="sxs-lookup"><span data-stu-id="bc0e5-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="bc0e5-157">Au début de la conception de cette page Web, nous avons fait un intérêt dans le fait que cette page est la meilleure pour une expérience de connexion rapide et fluide.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="bc0e5-158">Par conséquent, l’interface utilisateur qui est la plus visible dans le Flow est le champ nom d’utilisateur et mot de passe de la page de connexion pour une expérience d’entrée d’informations d’identification rapide.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="bc0e5-159">Bien que nous ayons identifié qu’il existe d’autres scénarios courants tels que la récupération du mot de passe et le référencement des déclarations de confidentialité, la riche expérience du Web est un meilleur emplacement pour ces expériences.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="bc0e5-160">Pour tous les flux qui ne sont pas liés à l’authentification Web sécurisée, nous vous recommandons de naviguer dans le navigateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="bc0e5-161">Cela est illustré dans l’exemple de fichier HTML (WebAuthLogin.html) comme suit : `<meta name="mswebdialog-newwindowurl" content="*" />` ouvre toutes les pages Web liées à à partir de la page de connexion ou d’autorisations dans le navigateur par défaut de l’utilisateur où l’utilisateur peut effectuer ces flux, puis revenir à l’application pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="bc0e5-162">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="bc0e5-162">Security Considerations</span></span>

<span data-ttu-id="bc0e5-163">Les articles suivants fournissent des conseils pour l’écriture de code C++ sécurisé.</span><span class="sxs-lookup"><span data-stu-id="bc0e5-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="bc0e5-164">Meilleures pratiques de sécurité pour C++</span><span class="sxs-lookup"><span data-stu-id="bc0e5-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="bc0e5-165">[Modèles & pratiques conseils de sécurité pour les applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="bc0e5-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc0e5-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc0e5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc0e5-167">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="bc0e5-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="bc0e5-168">Forum aux questions sur le Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="bc0e5-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="bc0e5-169">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="bc0e5-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="bc0e5-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="bc0e5-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

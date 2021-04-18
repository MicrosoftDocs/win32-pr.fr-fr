---
description: Un vecteur de version traite les commentaires conditionnels dans une page Web HTML. Autrement dit, les vecteurs de version vous permettent de créer un balisage basé sur la version du navigateur.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vecteurs de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321194"
---
# <a name="version-vectors"></a><span data-ttu-id="ebbd0-104">Vecteurs de version</span><span class="sxs-lookup"><span data-stu-id="ebbd0-104">Version Vectors</span></span>

<span data-ttu-id="ebbd0-105">Un *vecteur de version* traite les commentaires conditionnels dans une page Web HTML.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-105">A *version vector* processes conditional comments in an HTML webpage.</span></span> <span data-ttu-id="ebbd0-106">Autrement dit, les vecteurs de version vous permettent de créer un balisage basé sur la version du navigateur.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-106">That is, version vectors enable you to create markup based on the browser version.</span></span>

<span data-ttu-id="ebbd0-107">Considérez l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-107">Consider the following code example.</span></span>


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



<span data-ttu-id="ebbd0-108">Dans ce cas, si la version du navigateur Windows Internet Explorer est au moins 5,5, le paragraphe correspondant est affiché dans la page Web.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-108">In this case, if the Windows Internet Explorer browser version is at least 5.5, the corresponding paragraph is displayed in the webpage.</span></span> <span data-ttu-id="ebbd0-109">Bien que la première condition de cet exemple illustre la fonction des commentaires conditionnels, ces commentaires ne sont généralement pas utilisés pour afficher le balisage comme la première condition.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-109">Although the first condition in this example illustrates the function of conditional comments, these comments are not typically used to display markup like the first condition.</span></span> <span data-ttu-id="ebbd0-110">Au lieu de cela, les commentaires conditionnels restants dans l’exemple précédent sont plus courants.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-110">Instead, the remaining conditional comments in the previous example are more common.</span></span> <span data-ttu-id="ebbd0-111">Dans ces commentaires restants, les commentaires conditionnels utilisent une feuille de style différente pour chaque version différente du navigateur.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-111">In these remaining comments, the conditional comments use a different style sheet for each different version of the browser.</span></span>

<span data-ttu-id="ebbd0-112">L’exemple de code précédent vérifie également l’égalité pour Microsoft Internet Explorer 6 et Windows Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-112">The preceding code example also checks for equality for Microsoft Internet Explorer 6 and Windows Internet Explorer 7.</span></span> <span data-ttu-id="ebbd0-113">Mais pour Windows Internet Explorer 8, l’exemple utilise l’opérateur GTE (supérieur ou égal à).</span><span class="sxs-lookup"><span data-stu-id="ebbd0-113">But for Windows Internet Explorer 8, the example uses the gte operator (greater than or equal).</span></span> <span data-ttu-id="ebbd0-114">Cet opérateur aide à la prochaine épreuve l’exemple afin que la version la plus conforme à la norme de la feuille de style soit utilisée lorsqu’une nouvelle version du navigateur est libérée (au lieu d’utiliser une feuille de style ou aucune feuille de style incorrecte).</span><span class="sxs-lookup"><span data-stu-id="ebbd0-114">This operator helps future-proof the example so that the most standards-compliant version of the style sheet is used when a new version of the browser is released (instead of using the wrong style sheet or no style sheet).</span></span> <span data-ttu-id="ebbd0-115">Souvent, les applications existantes ne considèrent pas une version d’Internet Explorer antérieure à 7 (ou la version la plus récente d’Internet Explorer pour laquelle le site est conçu).</span><span class="sxs-lookup"><span data-stu-id="ebbd0-115">Existing applications often do not consider a version of Internet Explorer past 7 (or the newest version of Internet Explorer that the site is built for).</span></span> <span data-ttu-id="ebbd0-116">Pour plus d’informations sur les vecteurs de version, consultez [vecteurs de version](/previous-versions/cc817577(v=msdn.10)) dans MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-116">For more information about version vectors, see [Version Vectors](/previous-versions/cc817577(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebbd0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebbd0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebbd0-118">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="ebbd0-118">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 




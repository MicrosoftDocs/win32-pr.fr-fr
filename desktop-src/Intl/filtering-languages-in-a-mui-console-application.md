---
description: Une application console MUI peut prendre en charge les paramètres système ou les paramètres spécifiques à l’application pour ses langues d’interface utilisateur. Cette rubrique décrit le filtrage des langues pour ce type d’application.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrage des langues dans une application console MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865502"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="3ab8e-104">Filtrage des langues dans une application console MUI</span><span class="sxs-lookup"><span data-stu-id="3ab8e-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="3ab8e-105">Une application console MUI peut prendre en charge les paramètres système ou les paramètres spécifiques à l’application pour ses langues d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="3ab8e-106">Cette rubrique décrit le filtrage des langues pour ce type d’application.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="3ab8e-107">Limiter les langues à afficher</span><span class="sxs-lookup"><span data-stu-id="3ab8e-107">Limit the Languages to Display</span></span>

<span data-ttu-id="3ab8e-108">Contrairement à une fenêtre graphique, la console Windows ne peut pas afficher des [scripts complexes](uniscribe-glossary.md), tels que l’arabe, l’hébreu, le persan, l’hindi, l’ourdou, le thaï et bien d’autres.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="3ab8e-109">Par conséquent, la console ne peut en aucun cas afficher de nombreuses langues d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="3ab8e-110">La console peut afficher uniquement les caractères de la [page de codes OEM](code-pages.md) unique associée à la langue actuelle pour les applications non-Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="3ab8e-111">Pour chaque page de codes OEM, la console utilise une police particulière et cela peut ne pas fournir une couverture complète pour cette page de codes.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="3ab8e-112">Ces limitations liées à la console réduisent le nombre de langues de l’interface utilisateur que la console peut afficher sur un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="3ab8e-113">Par exemple, si la langue actuelle pour les applications non-Unicode est le japonais et que l’utilisateur essaie d’afficher du texte en allemand dans la console, les caractères avec les trémas ne s’affichent pas correctement.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="3ab8e-114">Si la langue actuelle pour les applications non-Unicode est l’allemand et que l’utilisateur souhaite afficher du texte en japonais dans la console, les résultats sont beaucoup pires, ce qui rend le texte presque incompréhensible.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="3ab8e-115">Lorsque vous fournissez une prise en charge de la console pour vos applications MUI, n’oubliez pas que la console fournit uniquement une prise en charge limitée des [éditeurs de méthode d’entrée](input-method-manager.md).</span><span class="sxs-lookup"><span data-stu-id="3ab8e-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="3ab8e-116">Définir la langue de la sortie de la console</span><span class="sxs-lookup"><span data-stu-id="3ab8e-116">Set the Language for Console Output</span></span>

<span data-ttu-id="3ab8e-117">Sur Windows Vista et versions ultérieures, une application console définit la langue pour prendre en charge l’affichage de la console en appelant [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="3ab8e-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="3ab8e-118">Dans cet appel, l’application transmet le \_ filtre de la console MUI \_ dans le paramètre *DwFlags* et la **valeur null** pour *pwszLanguagesBuffer*.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="3ab8e-119">Une alternative consiste à appeler [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) avec un identificateur de langue de 0.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="3ab8e-120">Ce paramètre force la fonction à sélectionner la langue qui prend le mieux en charge l’affichage de la console.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="3ab8e-121">Sur Windows XP, l’application peut uniquement définir la langue de sortie de la console en appelant [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) avec un identificateur de langue de 0.</span><span class="sxs-lookup"><span data-stu-id="3ab8e-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ab8e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ab8e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ab8e-123">Définition des préférences linguistiques de l’application</span><span class="sxs-lookup"><span data-stu-id="3ab8e-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 

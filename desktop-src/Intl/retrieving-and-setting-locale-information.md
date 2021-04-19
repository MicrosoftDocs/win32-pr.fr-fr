---
description: Récupération et définition des informations relatives aux paramètres régionaux
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Récupération et définition des informations relatives aux paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544647"
---
# <a name="retrieving-and-setting-locale-information"></a><span data-ttu-id="bc6ec-103">Récupération et définition des informations relatives aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="bc6ec-103">Retrieving and Setting Locale Information</span></span>

<span data-ttu-id="bc6ec-104">L’application doit être en mesure de récupérer et de définir des informations spécifiques sur [les paramètres régionaux et les langues](locales-and-languages.md)disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-104">The application must be able to retrieve and set specific information about available [locales and languages](locales-and-languages.md).</span></span> <span data-ttu-id="bc6ec-105">Chaque élément d’informations de paramètres régionaux, tel que le nom d’un jour spécifique de la semaine ou le caractère utilisé comme séparateur décimal, a une constante correspondante.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-105">Each element of locale information, such as the name of a particular day of the week or the character used as a decimal separator, has a corresponding constant.</span></span> <span data-ttu-id="bc6ec-106">Les constantes disponibles sont définies dans les [constantes d’informations de paramètres régionaux](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bc6ec-106">The available constants are defined in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="bc6ec-107">Votre application stocke et manipule toujours les informations de paramètres régionaux comme une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-107">Your application always stores and manipulates locale information as a null-terminated string.</span></span> <span data-ttu-id="bc6ec-108">Aucune donnée binaire n’est autorisée, et toutes les valeurs numériques doivent être spécifiées en tant que texte.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-108">No binary data is allowed, and any numeric values must be specified as text.</span></span> <span data-ttu-id="bc6ec-109">Chaque type d’informations a un format particulier.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-109">Each type of information has a particular format.</span></span> <span data-ttu-id="bc6ec-110">En outre, plusieurs types sont liés entre eux afin que la modification d’un type modifie également la valeur de l’autre type.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-110">Also, several types are linked together so that changing one type changes the value of the other type as well.</span></span>

<span data-ttu-id="bc6ec-111">Pour récupérer les informations relatives aux paramètres régionaux, l’application appelle [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante qui correspond aux informations requises.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-111">To retrieve locale information, the application calls [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with the constant that corresponds to the required information.</span></span> <span data-ttu-id="bc6ec-112">L’application peut appeler [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) pour définir un élément d’informations de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-112">The application can call [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) to set an item of locale information.</span></span>

> [!Note]  
> <span data-ttu-id="bc6ec-113">Bien qu’un [identificateur de paramètres régionaux](locale-identifiers.md) soit pris en charge, il n’est pas disponible pour une application, sauf si les paramètres régionaux correspondants sont également installés.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-113">Although a [locale identifier](locale-identifiers.md) might be supported, it is not available for use by an application unless the corresponding locale is also installed.</span></span>

 

<span data-ttu-id="bc6ec-114">Étant donné que la plupart des constantes d’informations de paramètres régionaux sont mutuellement exclusives, un seul type d’informations peut être géré à la fois.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-114">Since most locale information constants are mutually exclusive, only one type of information can be handled at a time.</span></span> <span data-ttu-id="bc6ec-115">Les exceptions à cette règle sont les [paramètres régionaux \_ use \_ CP \_ ACP](locale-use-cp-acp.md), [locale \_ \_ Number Number](locale-return-constants.md)et [locale \_ NOUSEROVERRIDE](locale-nouseroverride.md), qui peuvent être combinés avec d’autres constantes à l’aide d’un fichier binaire ou.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-115">The exceptions to this rule are [LOCALE\_USE\_CP\_ACP](locale-use-cp-acp.md), [LOCALE\_RETURN\_NUMBER](locale-return-constants.md), and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md), which can be combined with other constants using a binary OR.</span></span>

> [!Caution]  
> <span data-ttu-id="bc6ec-116">L’utilisation de paramètres régionaux \_ NOUSEROVERRIDE est fortement déconseillée, car elle désactive les préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-116">Use of LOCALE\_NOUSEROVERRIDE is strongly discouraged as it disables user preferences.</span></span>

 

<span data-ttu-id="bc6ec-117">Comme un certain nombre d’applications, par exemple Microsoft Active Directory, votre application peut conserver ses chaînes dans une base de données pouvant être triée.</span><span class="sxs-lookup"><span data-stu-id="bc6ec-117">Like a number of applications, for example Microsoft Active Directory, your application can maintain its strings in a sortable database.</span></span> <span data-ttu-id="bc6ec-118">Pour plus d’informations, consultez [gestion du tri dans vos applications](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bc6ec-118">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc6ec-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc6ec-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc6ec-120">Utilisation de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="bc6ec-120">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="bc6ec-121">Constantes d’informations de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="bc6ec-121">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="bc6ec-122">Gestion du tri dans vos applications</span><span class="sxs-lookup"><span data-stu-id="bc6ec-122">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="bc6ec-123">Utilisation de paramètres régionaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="bc6ec-123">Working with Custom Locales</span></span>](working-with-custom-locales.md)
</dt> </dl>

 

 




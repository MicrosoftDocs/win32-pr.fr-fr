---
description: Sur Windows Vista et versions ultérieures, vous pouvez utiliser des pseudo-paramètres régionaux pour tester l’adaptabilité des applications. Cette rubrique comprend des procédures pour l’utilisation de Pseudo-codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Utilisation de Pseudo-paramètres régionaux pour le test d’adaptabilité
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539761"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="4369f-104">Utilisation de Pseudo-paramètres régionaux pour le test d’adaptabilité</span><span class="sxs-lookup"><span data-stu-id="4369f-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="4369f-105">Les [Pseudo-paramètres régionaux](pseudo-locales.md) sont intégrés à Windows Vista et versions ultérieures, afin que vous puissiez y accéder via les API NLS (National Language Support).</span><span class="sxs-lookup"><span data-stu-id="4369f-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="4369f-106">Vous pouvez utiliser des pseudo-paramètres régionaux pour tester l' [adaptabilité](/windows/uwp/design/globalizing/globalizing-portal) de vos applications.</span><span class="sxs-lookup"><span data-stu-id="4369f-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="4369f-107">Cette rubrique comprend des procédures pour l’utilisation de Pseudo-codes.</span><span class="sxs-lookup"><span data-stu-id="4369f-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="4369f-108">Une tâche nécessitant une attention particulière en ce qui concerne les pseudo-paramètres régionaux consiste à les énumérer. Si vous êtes dans votre code, ou dans la partie Options régionales et linguistiques du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="4369f-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="4369f-109">Plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4369f-109">More on that later in this topic.</span></span>

<span data-ttu-id="4369f-110">Les noms des pseudo-paramètres régionaux sont « RPS-Ploc », « RPS-Ploca » et « RPS-plocm ».</span><span class="sxs-lookup"><span data-stu-id="4369f-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="4369f-111">À compter de Windows 10, les pseudo-paramètres régionaux « RPS-LATN-x-SH » sont également disponibles.</span><span class="sxs-lookup"><span data-stu-id="4369f-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="4369f-112">Récupérer les informations sur les pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="4369f-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="4369f-113">Vous pouvez utiliser [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) pour récupérer des informations sur les pseudo-paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="4369f-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="4369f-114">Transmettez à la fonction le nom des pseudo-paramètres régionaux particuliers (consultez la liste des noms ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="4369f-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="4369f-115">Par exemple, « RPS-plocm » pour les pseudo-paramètres régionaux en miroir.</span><span class="sxs-lookup"><span data-stu-id="4369f-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="4369f-116">Utiliser LocaleNameToLCID avec Pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="4369f-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="4369f-117">Vous pouvez appeler la fonction de mappage NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) avec le nom d’un pseudo-paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="4369f-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="4369f-118">Activer les pseudo-paramètres régionaux pour l’énumération</span><span class="sxs-lookup"><span data-stu-id="4369f-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="4369f-119">Dans votre application, vous pouvez appeler [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) pour énumérer les paramètres régionaux reconnus par le système.</span><span class="sxs-lookup"><span data-stu-id="4369f-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="4369f-120">La partie Options régionales et linguistiques du panneau de configuration appelle également **EnumSystemLocalesEx** pour générer la liste des paramètres régionaux qu’elle affiche.</span><span class="sxs-lookup"><span data-stu-id="4369f-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="4369f-121">Toutefois, par défaut, les quatre Pseudo-paramètres régionaux répertoriés ci-dessus ne sont pas reconnus par le système, donc ils ne sont pas retournés par **EnumSystemLocalesEx**.</span><span class="sxs-lookup"><span data-stu-id="4369f-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="4369f-122">Pour les systèmes Windows Vista jusqu’à Windows 10, version 1709, la solution consiste à activer les pseudo-paramètres régionaux en ajoutant des clés au registre Windows.</span><span class="sxs-lookup"><span data-stu-id="4369f-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="4369f-123">Les modifications sont apportées sous la \_ \_ clé nls du contrôle du système d’exploitation de la machine locale HKEY \\ \\ \\ \\ pour les langues installées sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4369f-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="4369f-124">Vous pouvez définir ces paramètres pour activer les pseudo-paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="4369f-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="4369f-125">Chaque clé indiquée ci-dessous est le LCID hexadécimal correspondant aux pseudo-paramètres régionaux en cours d’activation.</span><span class="sxs-lookup"><span data-stu-id="4369f-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="4369f-126">Chaque valeur est de type chaîne (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="4369f-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="4369f-127">Pour Windows 10, version 1803, la modification du Registre Windows comme celle-ci n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="4369f-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="4369f-128">Toutefois, vous pouvez toujours appeler les API NLS sans énumération avec les noms des pseudo-paramètres régionaux (voir les exemples de code ci-dessus) pour renseigner votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4369f-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4369f-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4369f-129">Related topics</span></span>

* [<span data-ttu-id="4369f-130">Utilisation de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="4369f-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="4369f-131">Pseudo-paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="4369f-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="4369f-132">EnumSystemLocalesEx</span><span class="sxs-lookup"><span data-stu-id="4369f-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="4369f-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="4369f-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="4369f-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="4369f-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)

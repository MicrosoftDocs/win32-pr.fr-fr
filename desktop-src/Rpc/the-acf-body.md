---
title: Corps ACF
description: Le corps ACF contient des attributs de configuration qui s’appliquent aux types et aux fonctions définis dans le corps de l’interface du fichier IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104032005"
---
# <a name="the-acf-body"></a><span data-ttu-id="1cbb0-103">Corps ACF</span><span class="sxs-lookup"><span data-stu-id="1cbb0-103">The ACF Body</span></span>

<span data-ttu-id="1cbb0-104">Le corps ACF contient des attributs de configuration qui s’appliquent aux types et aux fonctions définis dans le corps de l’interface du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="1cbb0-105">Le corps du CCP peut être vide ou peut contenir des attributs d' [**inclusion**](/windows/desktop/Midl/include), de [**typedef**](/windows/desktop/Midl/typedef), de fonction et de paramètre ACF.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="1cbb0-106">Tous ces éléments sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-106">All of these items are optional.</span></span> <span data-ttu-id="1cbb0-107">Les attributs appliqués aux types et aux fonctions individuels dans le corps CCP remplacent les attributs dans l’en-tête ACF.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="1cbb0-108">Le ACF spécifie le comportement sur l’ordinateur local et n’affecte pas les données transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="1cbb0-109">Il est utilisé pour spécifier les détails d’un stub à générer.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="1cbb0-110">En mode de compatibilité DCE ([**/OSF**](/windows/desktop/Midl/-osf)), le ACF n’affecte pas l’interaction entre les stubs, mais entre le stub et le code d’application.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="1cbb0-111">Un paramètre spécifié dans le CCP doit être l’un des paramètres spécifiés dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="1cbb0-112">L’ordre de spécification du paramètre dans le ACF n’est pas significatif, car la correspondance est par nom, et non par position.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="1cbb0-113">La liste de paramètres dans le CCP peut être vide, même si la liste de paramètres de la signature IDL correspondante n’est pas (mais cela n’est pas recommandé).</span><span class="sxs-lookup"><span data-stu-id="1cbb0-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="1cbb0-114">Les déclarateurs abstraits (paramètres sans nom) dans le fichier IDL font en sorte que le compilateur MIDL signale des erreurs lors du traitement du CCP, car le paramètre est introuvable.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="1cbb0-115">La directive CCP **include** spécifie les fichiers d’en-tête à afficher dans l’en-tête généré dans le cadre d’une instruction **\# include** C-preprocesseur standard.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="1cbb0-116">Le mot clé ACF **include** est différent d’une directive **\# include** .</span><span class="sxs-lookup"><span data-stu-id="1cbb0-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="1cbb0-117">Le mot clé ACF **include** entraîne l’affichage de la ligne «**\# include** *filename*» dans le fichier d’en-tête généré, tandis que la directive C «**\# include** *filename*» provoque le placement du contenu de ce fichier dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="1cbb0-118">L’instruction CCP [**typedef**](/windows/desktop/Midl/typedef) vous permet d’appliquer des attributs de type ACF aux types précédemment définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="1cbb0-119">La syntaxe de **typedef** ACF diffère de la syntaxe C **typedef** .</span><span class="sxs-lookup"><span data-stu-id="1cbb0-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="1cbb0-120">Les attributs de fonction ACF vous permettent de spécifier des attributs qui s’appliquent à la fonction dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="1cbb0-121">Pour plus d’informations, consultez **\[** [**code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** et **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1cbb0-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="1cbb0-122">Les attributs de paramètres ACF vous permettent de spécifier des attributs qui s’appliquent à des paramètres individuels de la fonction.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="1cbb0-123">Pour plus d’informations, consultez **\[** [**\_ nombre d’octets**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1cbb0-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cbb0-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1cbb0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cbb0-125">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="1cbb0-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="1cbb0-127">[**\[\_handle automatique\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="1cbb0-128">[**\[code\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="1cbb0-129">[**\[\_handle explicite\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="1cbb0-130">Fichier IDL (Interface Definition Language)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="1cbb0-131">[**\[handle implicite \_\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="1cbb0-132">**inclusion**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="1cbb0-133">compilateur</span><span class="sxs-lookup"><span data-stu-id="1cbb0-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="1cbb0-134">[**\[SansCode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="1cbb0-135">[**\[requêtes\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="1cbb0-136">[**\[représenter \_ comme\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="1cbb0-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 
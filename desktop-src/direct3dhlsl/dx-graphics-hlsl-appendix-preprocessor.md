---
title: Directives de préprocesseur (HLSL)
description: Les directives de préprocesseur, telles que \ define et \ ifdef, sont généralement utilisées pour rendre les programmes sources faciles à modifier et à compiler dans différents environnements d’exécution.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386828"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="f574e-103">Directives de préprocesseur (HLSL)</span><span class="sxs-lookup"><span data-stu-id="f574e-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="f574e-104">Les directives de préprocesseur, telles que [ \# define](dx-graphics-hlsl-appendix-pre-define.md) et [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), sont généralement utilisées pour rendre les programmes sources faciles à modifier et à compiler dans différents environnements d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f574e-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="f574e-105">Les directives contenues dans le fichier source indiquent au préprocesseur d'exécuter des actions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f574e-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="f574e-106">Par exemple, le préprocesseur peut remplacer des jetons dans le texte, insérer le contenu d'autres fichiers dans le fichier source ou supprimer la compilation d'une partie du fichier en supprimant des sections de texte.</span><span class="sxs-lookup"><span data-stu-id="f574e-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="f574e-107">Les lignes de préprocesseur sont reconnues et exécutées avant l'expansion macro.</span><span class="sxs-lookup"><span data-stu-id="f574e-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="f574e-108">Par conséquent, si une macro se développe en quelque chose qui ressemble à une commande de préprocesseur, cette commande n'est pas reconnue par le préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="f574e-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="f574e-109">Les déclarations de préprocesseur utilisent le même jeu de caractères que les instructions de fichier source, sauf que les séquences d'échappement ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f574e-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="f574e-110">Le jeu de caractères utilisé dans les instructions de préprocesseur est identique au jeu de caractères d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f574e-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="f574e-111">Le préprocesseur reconnaît aussi les valeurs de caractères négatives.</span><span class="sxs-lookup"><span data-stu-id="f574e-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="f574e-112">Le préprocesseur HLSL reconnaît les directives suivantes :</span><span class="sxs-lookup"><span data-stu-id="f574e-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="f574e-113">\#définition</span><span class="sxs-lookup"><span data-stu-id="f574e-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="f574e-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="f574e-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f574e-115">\#else</span><span class="sxs-lookup"><span data-stu-id="f574e-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f574e-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="f574e-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f574e-117">\#Erreurs</span><span class="sxs-lookup"><span data-stu-id="f574e-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="f574e-118">\#que</span><span class="sxs-lookup"><span data-stu-id="f574e-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="f574e-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="f574e-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="f574e-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="f574e-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="f574e-121">\#inclusion</span><span class="sxs-lookup"><span data-stu-id="f574e-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="f574e-122">\#line</span><span class="sxs-lookup"><span data-stu-id="f574e-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="f574e-123">\#Bali</span><span class="sxs-lookup"><span data-stu-id="f574e-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="f574e-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="f574e-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="f574e-125">Le signe dièse ( \# ) doit être le premier caractère autre qu’un espace blanc sur la ligne contenant la directive ; les espaces blancs peuvent apparaître entre le signe dièse et la première lettre de la directive.</span><span class="sxs-lookup"><span data-stu-id="f574e-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="f574e-126">Certaines directives incluent des arguments ou des valeurs.</span><span class="sxs-lookup"><span data-stu-id="f574e-126">Some directives include arguments or values.</span></span> <span data-ttu-id="f574e-127">Tout texte qui suit une directive (sauf un argument ou une valeur qui fait partie de la directive) doit être précédé du délimiteur de commentaire sur une seule ligne (//) ou placé entre les délimiteurs de commentaires (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="f574e-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="f574e-128">Les lignes contenant des directives de préprocesseur peuvent être poursuivies en faisant immédiatement précéder le marqueur de fin de ligne d’une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f574e-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="f574e-129">Les directives de préprocesseur peuvent apparaître n'importe où dans un fichier source, mais elles s'appliquent uniquement au reste du fichier source.</span><span class="sxs-lookup"><span data-stu-id="f574e-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f574e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f574e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f574e-131">Annexe (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f574e-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 





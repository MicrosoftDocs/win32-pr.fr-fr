---
description: NTFS stocke les noms de fichiers au format Unicode. En revanche, les anciens systèmes de fichiers FAT12, FAT16 et FAT32 utilisent le jeu de caractères OEM. Pour plus d'informations, consultez Pages de codes.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Jeux de caractères utilisés dans les noms de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866105"
---
# <a name="character-sets-used-in-file-names"></a><span data-ttu-id="50f28-105">Jeux de caractères utilisés dans les noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="50f28-105">Character Sets Used in File Names</span></span>

<span data-ttu-id="50f28-106">NTFS stocke les noms de fichiers au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="50f28-106">NTFS stores file names in Unicode.</span></span> <span data-ttu-id="50f28-107">En revanche, les anciens systèmes de fichiers FAT12, FAT16 et FAT32 utilisent le jeu de caractères OEM.</span><span class="sxs-lookup"><span data-stu-id="50f28-107">In contrast, the older FAT12, FAT16, and FAT32 file systems use the OEM character set.</span></span> <span data-ttu-id="50f28-108">Pour plus d’informations, consultez [Pages de codes](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="50f28-108">For more information, see [Code Pages](code-pages.md).</span></span>

<span data-ttu-id="50f28-109">Les applications non-Unicode qui créent des fichiers FAT doivent parfois utiliser les fonctions de conversion de la bibliothèque Runtime C standard pour effectuer la conversion entre le jeu de caractères de page de codes Windows et le jeu de caractères de la page de codes OEM.</span><span class="sxs-lookup"><span data-stu-id="50f28-109">Non-Unicode applications that create FAT files sometimes have to use the standard C runtime library conversion functions to translate between the Windows code page character set and the OEM code page character set.</span></span> <span data-ttu-id="50f28-110">Avec les implémentations Unicode des fonctions du système de fichiers, il n’est pas nécessaire d’effectuer de telles traductions.</span><span class="sxs-lookup"><span data-stu-id="50f28-110">With Unicode implementations of the file system functions, it is not necessary to perform such translations.</span></span>

<span data-ttu-id="50f28-111">Votre application peut utiliser des types de chaîne génériques, comme décrit dans [types de données Windows pour les chaînes](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="50f28-111">Your application can use generic string types, as described in [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span> <span data-ttu-id="50f28-112">L’application peut également utiliser des prototypes de fonctions génériques à l’aide de techniques décrites dans [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="50f28-112">The application can also use generic function prototypes using techniques described in [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span> <span data-ttu-id="50f28-113">Pour les types de chaîne génériques ou les prototypes de fonction génériques, votre application peut utiliser un fichier source unique pour compiler une version Unicode ou non-Unicode.</span><span class="sxs-lookup"><span data-stu-id="50f28-113">For either generic string types or generic function prototypes, your application can use a single source file to compile either a Unicode or a non-Unicode version.</span></span> <span data-ttu-id="50f28-114">Pour ce faire, l’application fournit des macros pour les fonctions qui ne sont pas appelées lors de la compilation pour Unicode.</span><span class="sxs-lookup"><span data-stu-id="50f28-114">To allow for this, the application provides macros for functions that are not invoked when compiling for Unicode.</span></span>

<span data-ttu-id="50f28-115">Dans les systèmes de fichiers NTFS et FAT, les caractères spéciaux sont les suivants : ' \\ ', '/', '. ', ' ? 'et' \* '.</span><span class="sxs-lookup"><span data-stu-id="50f28-115">In both NTFS and FAT file systems, the special file name characters are: '\\', '/', '.', '?', and '\*'.</span></span> <span data-ttu-id="50f28-116">Sur les pages de codes OEM, ces caractères spéciaux se trouvent dans la plage de caractères ASCII (0x00 à 0x7F).</span><span class="sxs-lookup"><span data-stu-id="50f28-116">On OEM code pages, these special characters are in the ASCII range of characters (0x00 through 0x7F).</span></span> <span data-ttu-id="50f28-117">Leurs équivalents Unicode ont les mêmes valeurs dans une forme de 2 octets, 0x0000 à 0x007F.</span><span class="sxs-lookup"><span data-stu-id="50f28-117">Their Unicode equivalents are the same values in a 2-byte form, 0x0000 through 0x007F.</span></span>

> [!Caution]  
> <span data-ttu-id="50f28-118">La page de codes Windows et les jeux de caractères de la page de codes OEM utilisés sur les systèmes d’exploitation en langue japonaise contiennent le symbole yen (¥) au lieu d’une barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="50f28-118">Windows code page and OEM code page character sets used on Japanese-language operating systems contain the Yen symbol (¥) instead of a backslash (\\).</span></span> <span data-ttu-id="50f28-119">Ainsi, le symbole yen est un caractère interdit pour les systèmes de fichiers NTFS et FAT.</span><span class="sxs-lookup"><span data-stu-id="50f28-119">Thus, the Yen symbol is a prohibited character for NTFS and FAT file systems.</span></span> <span data-ttu-id="50f28-120">Lors du mappage Unicode sur une page de codes de langue japonaise, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) et d’autres fonctions de conversion mappent la barre oblique inverse (u + 005C) et le symbole de yen Unicode normal (u + 00A5) sur ce même caractère.</span><span class="sxs-lookup"><span data-stu-id="50f28-120">When mapping Unicode to a Japanese-language code page, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and other conversion functions map both backslash (U+005C) and the normal Unicode Yen symbol (U+00A5) to this same character.</span></span> <span data-ttu-id="50f28-121">Pour des raisons de sécurité, les applications ne doivent pas, en général, autoriser le caractère U + 00A5 dans une chaîne Unicode qui peut être convertie pour être utilisée comme nom de fichier FAT.</span><span class="sxs-lookup"><span data-stu-id="50f28-121">For security reasons, your applications should not typically allow the character U+00A5 in a Unicode string that might be converted for use as a FAT file name.</span></span> <span data-ttu-id="50f28-122">Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="50f28-122">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="50f28-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50f28-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f28-124">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="50f28-124">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> <dt>

[<span data-ttu-id="50f28-125">Considérations relatives à la sécurité : fonctionnalités internationales</span><span class="sxs-lookup"><span data-stu-id="50f28-125">Security Considerations: International Features</span></span>](security-considerations--international-features.md)
</dt> </dl>

 

 




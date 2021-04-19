---
description: Quand une application convertit des chaînes ASCII ou d’une page de codes Windows (ANSI) en Unicode, elle doit convertir les séquences d’échappement caractère par caractère en Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Utilisation de séquences d’échappement et de caractères de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531415"
---
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="3d50d-103">Utilisation de séquences d’échappement et de caractères de contrôle</span><span class="sxs-lookup"><span data-stu-id="3d50d-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="3d50d-104">Quand une application convertit des chaînes ASCII ou d’une [page de codes Windows (ANSI)](code-pages.md) en Unicode, elle doit convertir les séquences d’échappement caractère par caractère en Unicode.</span><span class="sxs-lookup"><span data-stu-id="3d50d-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="3d50d-105">Lorsqu’un fichier texte ASCII ou d’un autre fichier texte 8 bits est converti en Unicode, il est possible qu’il soit reconverti par la suite.</span><span class="sxs-lookup"><span data-stu-id="3d50d-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="3d50d-106">La conversion de séquences d’échappement en Unicode caractère par caractère, au lieu de les combiner comme un caractère Unicode unique, permet d’effectuer la conversion inverse sans avoir besoin de reconnaître et d’analyser les séquences d’échappement comme telles.</span><span class="sxs-lookup"><span data-stu-id="3d50d-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="3d50d-107">Par exemple, ESC + A doit devenir 0x001B (ESC), 0x0041 (A), au lieu de 0x411B.</span><span class="sxs-lookup"><span data-stu-id="3d50d-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="3d50d-108">Les premières valeurs de code 32 16 bits en Unicode sont destinées aux caractères de contrôle 32.</span><span class="sxs-lookup"><span data-stu-id="3d50d-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="3d50d-109">Cette spécification prend en charge l’utilisation existante de caractères de contrôle à des fins de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="3d50d-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="3d50d-110">Les applications Unicode peuvent traiter ces caractères de contrôle exactement de la même façon qu’ils traitent leurs équivalents ASCII.</span><span class="sxs-lookup"><span data-stu-id="3d50d-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d50d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d50d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d50d-112">Utilisation de caractères spéciaux en Unicode</span><span class="sxs-lookup"><span data-stu-id="3d50d-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 




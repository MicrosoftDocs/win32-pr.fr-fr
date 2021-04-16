---
title: LANGUAGE (instruction)
description: Définit la langue de toutes les ressources jusqu’à l’instruction de langage suivante ou jusqu’à la fin du fichier.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menus de l’instruction de langage et autres ressources
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507910"
---
# <a name="language-statement"></a><span data-ttu-id="f1d12-104">LANGUAGE (instruction)</span><span class="sxs-lookup"><span data-stu-id="f1d12-104">LANGUAGE statement</span></span>

<span data-ttu-id="f1d12-105">Définit la langue de toutes les ressources jusqu’à l’instruction de **langage** suivante ou jusqu’à la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="f1d12-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="f1d12-106">Lorsque l’instruction **Language** apparaît avant le début du corps d’une définition de ressource [**accélérateurs**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , la langue spécifiée s’applique uniquement à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="f1d12-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="f1d12-107"><span id="language"></span><span id="LANGUAGE"></span>*sous*</span><span class="sxs-lookup"><span data-stu-id="f1d12-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="f1d12-108">Identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="f1d12-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f1d12-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sous-langue*</span><span class="sxs-lookup"><span data-stu-id="f1d12-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="f1d12-110">Identificateur de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="f1d12-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="f1d12-111">Pour plus d’informations, consultez [constantes et chaînes](/windows/desktop/Intl/language-identifier-constants-and-strings)de l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="f1d12-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="f1d12-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1d12-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d12-113">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="f1d12-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="f1d12-114">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="f1d12-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="f1d12-115">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="f1d12-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="f1d12-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="f1d12-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="f1d12-117">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="f1d12-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="f1d12-118">**Version**</span><span class="sxs-lookup"><span data-stu-id="f1d12-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
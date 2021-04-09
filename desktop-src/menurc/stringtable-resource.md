---
title: Ressource STRINGTABLE
description: Définit une ou plusieurs ressources de type chaîne pour une application. Les ressources de type chaîne sont simplement des chaînes Unicode ou ASCII se terminant par un caractère null qui peuvent être chargées quand cela est nécessaire à partir du fichier exécutable, à l’aide de la fonction LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menus des ressources STRINGTABLE et autres ressources
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101628"
---
# <a name="stringtable-resource"></a><span data-ttu-id="7db73-105">Ressource STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="7db73-105">STRINGTABLE resource</span></span>

<span data-ttu-id="7db73-106">Définit une ou plusieurs ressources de type chaîne pour une application.</span><span class="sxs-lookup"><span data-stu-id="7db73-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="7db73-107">Les ressources de type chaîne sont simplement des chaînes Unicode ou ASCII se terminant par un caractère null qui peuvent être chargées quand cela est nécessaire à partir du fichier exécutable, à l’aide de la fonction [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .</span><span class="sxs-lookup"><span data-stu-id="7db73-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="7db73-108">Il existe deux façons de mettre en forme une instruction **STRINGTABLE** :</span><span class="sxs-lookup"><span data-stu-id="7db73-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="7db73-109">\- ou -</span><span class="sxs-lookup"><span data-stu-id="7db73-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="7db73-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7db73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db73-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*</span><span class="sxs-lookup"><span data-stu-id="7db73-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="7db73-112">Ce paramètre peut être égal à zéro ou plusieurs des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="7db73-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="7db73-113">.</span><span class="sxs-lookup"><span data-stu-id="7db73-113">Statement</span></span>                                                        | <span data-ttu-id="7db73-114">Description</span><span class="sxs-lookup"><span data-stu-id="7db73-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db73-115">[**Caractéristiques**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7db73-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="7db73-116">Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="7db73-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="7db73-117">Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7db73-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="7db73-118">[](language-statement.md) *Langue* langue, sous- *langue*</span><span class="sxs-lookup"><span data-stu-id="7db73-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="7db73-119">Spécifie la langue de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7db73-119">Specifies the language for the resource.</span></span> <span data-ttu-id="7db73-120">Pour plus d’informations, consultez [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7db73-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="7db73-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7db73-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="7db73-122">Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources.</span><span class="sxs-lookup"><span data-stu-id="7db73-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="7db73-123">Pour plus d’informations, consultez [**version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7db73-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="7db73-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="7db73-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="7db73-125">Entier non signé 16 bits qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="7db73-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7db73-126"><span id="string"></span><span id="STRING"></span>*chaîne*</span><span class="sxs-lookup"><span data-stu-id="7db73-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="7db73-127">Une ou plusieurs chaînes, placées entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="7db73-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="7db73-128">La chaîne ne doit pas dépasser 4097 caractères et doit occuper une seule ligne dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="7db73-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="7db73-129">Pour ajouter un retour chariot à la chaîne, utilisez la séquence de caractères suivante : \\ 012.</span><span class="sxs-lookup"><span data-stu-id="7db73-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="7db73-130">Par exemple, « ligne un \\ 012Line deux » définit une chaîne qui s’affiche comme suit :</span><span class="sxs-lookup"><span data-stu-id="7db73-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="7db73-131">Pour incorporer des guillemets dans la chaîne, utilisez la séquence suivante : "".</span><span class="sxs-lookup"><span data-stu-id="7db73-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="7db73-132">Par exemple, "" ", ligne trois" ", définit une chaîne qui s’affiche comme suit :</span><span class="sxs-lookup"><span data-stu-id="7db73-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="7db73-133">Pour encoder des caractères Unicode, utilisez un « L » suivi des caractères Unicode encadrés par des guillemets.</span><span class="sxs-lookup"><span data-stu-id="7db73-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="7db73-134">Pour obtenir un exemple, consultez la section exemples.</span><span class="sxs-lookup"><span data-stu-id="7db73-134">See the Examples section for an example.</span></span>

<span data-ttu-id="7db73-135">Le compilateur de ressources prend également en charge les continuations de ligne dans *String*.</span><span class="sxs-lookup"><span data-stu-id="7db73-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="7db73-136">Pour obtenir un exemple, consultez la section exemples.</span><span class="sxs-lookup"><span data-stu-id="7db73-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="7db73-137">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="7db73-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7db73-138">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7db73-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7db73-139">Notes</span><span class="sxs-lookup"><span data-stu-id="7db73-139">Remarks</span></span>

<span data-ttu-id="7db73-140">RC alloue 16 chaînes par section et utilise la valeur d’identificateur pour déterminer la section qui doit contenir la chaîne.</span><span class="sxs-lookup"><span data-stu-id="7db73-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="7db73-141">Les chaînes dont les identificateurs diffèrent uniquement dans les 4 bits inférieurs sont placées dans la même section.</span><span class="sxs-lookup"><span data-stu-id="7db73-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="7db73-142">Pour plus d’informations, consultez [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="7db73-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="7db73-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="7db73-143">Examples</span></span>

<span data-ttu-id="7db73-144">L’exemple suivant illustre l’utilisation de l’instruction **STRINGTABLE** pour afficher des chaînes ASCII :</span><span class="sxs-lookup"><span data-stu-id="7db73-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="7db73-145">L’exemple suivant montre comment encoder des caractères Unicode :</span><span class="sxs-lookup"><span data-stu-id="7db73-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="7db73-146">L’exemple suivant montre des chaînes avec ASCII et Unicode.</span><span class="sxs-lookup"><span data-stu-id="7db73-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="7db73-147">Notez que les chaînes sans la « L » initiale utilisent le format d’échappement à 2 chiffres :</span><span class="sxs-lookup"><span data-stu-id="7db73-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="7db73-148">L’exemple suivant montre comment les continuations de ligne peuvent être utilisées :</span><span class="sxs-lookup"><span data-stu-id="7db73-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="7db73-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7db73-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db73-150">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="7db73-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="7db73-151">**ACCÉLÉRATEURS**</span><span class="sxs-lookup"><span data-stu-id="7db73-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="7db73-152">**ATTRIBUTS**</span><span class="sxs-lookup"><span data-stu-id="7db73-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="7db73-153">**SOUS**</span><span class="sxs-lookup"><span data-stu-id="7db73-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="7db73-154">**MENUS**</span><span class="sxs-lookup"><span data-stu-id="7db73-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7db73-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="7db73-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="7db73-156">**Version**</span><span class="sxs-lookup"><span data-stu-id="7db73-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
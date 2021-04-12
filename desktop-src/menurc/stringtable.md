---
title: StringTable, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de mise en forme de la langue et de la page de codes pour les chaînes spécifiées par le membre Children. Une page de codes est un jeu de caractères ordonné.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- Menus de la structure StringTable et autres ressources
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384140"
---
# <a name="stringtable-structure"></a><span data-ttu-id="25c2b-106">StringTable, structure</span><span class="sxs-lookup"><span data-stu-id="25c2b-106">StringTable structure</span></span>

<span data-ttu-id="25c2b-107">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="25c2b-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="25c2b-108">Elle contient des informations de mise en forme de la langue et de la page de codes pour les chaînes spécifiées par le membre **Children** .</span><span class="sxs-lookup"><span data-stu-id="25c2b-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="25c2b-109">Une page de codes est un jeu de caractères ordonné.</span><span class="sxs-lookup"><span data-stu-id="25c2b-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c2b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25c2b-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="25c2b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="25c2b-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="25c2b-112">**wLength**</span><span class="sxs-lookup"><span data-stu-id="25c2b-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-113">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="25c2b-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-114">Longueur, en octets, de cette structure **STRINGTABLE** , y compris toutes les structures indiquées par le membre **Children** .</span><span class="sxs-lookup"><span data-stu-id="25c2b-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="25c2b-115">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="25c2b-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-116">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="25c2b-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-117">Ce membre est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="25c2b-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="25c2b-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="25c2b-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-119">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="25c2b-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-120">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="25c2b-120">The type of data in the version resource.</span></span> <span data-ttu-id="25c2b-121">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="25c2b-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="25c2b-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="25c2b-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-123">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="25c2b-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-124">Nombre hexadécimal à 8 chiffres stocké sous la forme d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="25c2b-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="25c2b-125">Les quatre chiffres les plus significatifs représentent l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="25c2b-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="25c2b-126">Les quatre chiffres les moins significatifs représentent la page de codes pour laquelle les données sont mises en forme.</span><span class="sxs-lookup"><span data-stu-id="25c2b-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="25c2b-127">Chaque identificateur de langue Microsoft standard contient deux parties : les 10 bits de poids faible spécifient la langue principale et les 6 bits de poids fort spécifient la sous-langue.</span><span class="sxs-lookup"><span data-stu-id="25c2b-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="25c2b-128">Pour obtenir une table des identificateurs valides, consultez.</span><span class="sxs-lookup"><span data-stu-id="25c2b-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="25c2b-129">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="25c2b-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-130">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="25c2b-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-131">Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="25c2b-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="25c2b-132">**Children**</span><span class="sxs-lookup"><span data-stu-id="25c2b-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="25c2b-133">Type : **[ **chaîne**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="25c2b-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="25c2b-134">Tableau d’une ou de plusieurs structures de [**chaîne**](string-str.md) .</span><span class="sxs-lookup"><span data-stu-id="25c2b-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25c2b-135">Notes</span><span class="sxs-lookup"><span data-stu-id="25c2b-135">Remarks</span></span>

<span data-ttu-id="25c2b-136">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="25c2b-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="25c2b-137">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="25c2b-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="25c2b-138">Le membre **Children** de la structure [**StringFileInfo**](stringfileinfo.md) contient au moins une structure **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="25c2b-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="25c2b-139">Définissez la partie page de codes du membre **szKey** sur la valeur hexadécimale 0x04b0 pour indiquer la page de codes Unicode, ou sur la valeur hexadécimale de la page de codes appropriée pour le composant de langage.</span><span class="sxs-lookup"><span data-stu-id="25c2b-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="25c2b-140">Une fois que vous avez choisi la valeur de la page de codes, vous devez continuer à utiliser la même valeur dans les révisions ultérieures du fichier.</span><span class="sxs-lookup"><span data-stu-id="25c2b-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="25c2b-141">Un fichier exécutable ou une DLL qui prend en charge plusieurs langages doit avoir une ressource de version pour chaque langue, plutôt qu’une ressource de version unique qui contient des chaînes dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="25c2b-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="25c2b-142">Toutefois, si vous utilisez la structure [**var**](var-str.md) pour répertorier les langues prises en charge par votre application, le nombre de structures **STRINGTABLE** dans la ressource de version est directement lié au nombre de paires d’identificateurs de langue ou de page de code dans le membre **value** de la structure **var** .</span><span class="sxs-lookup"><span data-stu-id="25c2b-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c2b-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25c2b-143">Requirements</span></span>



| <span data-ttu-id="25c2b-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25c2b-144">Requirement</span></span> | <span data-ttu-id="25c2b-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="25c2b-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="25c2b-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c2b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="25c2b-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c2b-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="25c2b-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25c2b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="25c2b-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25c2b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="25c2b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c2b-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="25c2b-151">**Référence**</span><span class="sxs-lookup"><span data-stu-id="25c2b-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25c2b-152">**String**</span><span class="sxs-lookup"><span data-stu-id="25c2b-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="25c2b-153">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="25c2b-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="25c2b-154">**Var**</span><span class="sxs-lookup"><span data-stu-id="25c2b-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="25c2b-155">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="25c2b-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="25c2b-156">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="25c2b-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="25c2b-157">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="25c2b-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25c2b-158">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="25c2b-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






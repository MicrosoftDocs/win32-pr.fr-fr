---
title: StringFileInfo, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations de version qui peuvent être affichées pour une langue et une page de codes particulières.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Menus de la structure StringFileInfo et autres ressources
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941801"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="9795e-105">StringFileInfo, structure</span><span class="sxs-lookup"><span data-stu-id="9795e-105">StringFileInfo structure</span></span>

<span data-ttu-id="9795e-106">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="9795e-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="9795e-107">Elle contient des informations de version qui peuvent être affichées pour une langue et une page de codes particulières.</span><span class="sxs-lookup"><span data-stu-id="9795e-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="9795e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9795e-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="9795e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9795e-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9795e-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="9795e-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="9795e-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-112">Longueur, en octets, du bloc **StringFileInfo** entier, y compris toutes les structures indiquées par le membre **Children** .</span><span class="sxs-lookup"><span data-stu-id="9795e-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="9795e-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="9795e-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="9795e-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-115">Ce membre est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9795e-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9795e-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="9795e-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-117">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="9795e-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-118">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="9795e-118">The type of data in the version resource.</span></span> <span data-ttu-id="9795e-119">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="9795e-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="9795e-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="9795e-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-121">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="9795e-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-122">Chaîne Unicode L "StringFileInfo".</span><span class="sxs-lookup"><span data-stu-id="9795e-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="9795e-123">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="9795e-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="9795e-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-125">Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9795e-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="9795e-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="9795e-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="9795e-127">Type : **[ **STRINGTABLE**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="9795e-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9795e-128">Tableau d’une ou de plusieurs structures [**STRINGTABLE**](stringtable.md) .</span><span class="sxs-lookup"><span data-stu-id="9795e-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="9795e-129">Chaque membre **szKey** de la structure **STRINGTABLE** indique la langue et la page de codes appropriées pour l’affichage du texte dans cette structure **STRINGTABLE** .</span><span class="sxs-lookup"><span data-stu-id="9795e-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9795e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9795e-130">Remarks</span></span>

<span data-ttu-id="9795e-131">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="9795e-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="9795e-132">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="9795e-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="9795e-133">Le membre **Children** de la structure de [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) peut contenir zéro ou plusieurs structures **StringFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="9795e-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9795e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9795e-134">Requirements</span></span>



| <span data-ttu-id="9795e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9795e-135">Requirement</span></span> | <span data-ttu-id="9795e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9795e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="9795e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9795e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9795e-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9795e-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9795e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9795e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9795e-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9795e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9795e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9795e-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="9795e-142">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9795e-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9795e-143">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="9795e-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="9795e-144">**String**</span><span class="sxs-lookup"><span data-stu-id="9795e-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="9795e-145">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="9795e-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="9795e-146">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9795e-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9795e-147">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="9795e-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






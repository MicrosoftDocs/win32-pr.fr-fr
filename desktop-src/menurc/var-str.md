---
title: Var, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Il contient généralement une liste de paires de langue et d’identificateur de page de codes que la version de l’application ou de la DLL prend en charge.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Menus de structure var et autres ressources
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844298"
---
# <a name="var-structure"></a><span data-ttu-id="aac07-105">Var, structure</span><span class="sxs-lookup"><span data-stu-id="aac07-105">Var structure</span></span>

<span data-ttu-id="aac07-106">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="aac07-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="aac07-107">Il contient généralement une liste de paires de langue et d’identificateur de page de codes que la version de l’application ou de la DLL prend en charge.</span><span class="sxs-lookup"><span data-stu-id="aac07-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac07-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aac07-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="aac07-109">Membres</span><span class="sxs-lookup"><span data-stu-id="aac07-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="aac07-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="aac07-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="aac07-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-112">Longueur, en octets, de la structure **var** .</span><span class="sxs-lookup"><span data-stu-id="aac07-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="aac07-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="aac07-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-115">Longueur, en octets, du membre de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="aac07-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="aac07-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-117">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="aac07-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-118">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="aac07-118">The type of data in the version resource.</span></span> <span data-ttu-id="aac07-119">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="aac07-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="aac07-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-121">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="aac07-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-122">Chaîne Unicode L « translation ».</span><span class="sxs-lookup"><span data-stu-id="aac07-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="aac07-123">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="aac07-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="aac07-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-125">Autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aac07-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-126">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="aac07-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="aac07-127">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="aac07-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="aac07-128">Tableau d’une ou de plusieurs valeurs qui sont des paires d’identificateurs de page de codes et de langage.</span><span class="sxs-lookup"><span data-stu-id="aac07-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="aac07-129">Pour plus d’informations, consultez la section Notes suivante.</span><span class="sxs-lookup"><span data-stu-id="aac07-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aac07-130">Notes</span><span class="sxs-lookup"><span data-stu-id="aac07-130">Remarks</span></span>

<span data-ttu-id="aac07-131">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="aac07-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="aac07-132">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="aac07-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="aac07-133">Si vous utilisez la structure **var** pour répertorier les langues prises en charge par votre application ou dll au lieu d’utiliser plusieurs ressources de version, utilisez le membre **value** pour contenir un tableau de valeurs **DWORD** indiquant les combinaisons de langue et de page de codes prises en charge par ce fichier.</span><span class="sxs-lookup"><span data-stu-id="aac07-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="aac07-134">Le mot de poids faible de chaque **DWORD** doit contenir un identificateur de langue Microsoft, et le mot de poids fort doit contenir le numéro de page de codes IBM.</span><span class="sxs-lookup"><span data-stu-id="aac07-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="aac07-135">Le mot de poids fort ou de poids faible peut être égal à zéro, ce qui indique que le fichier est indépendant de la langue ou de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="aac07-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="aac07-136">Si la structure **var** est omise, le fichier est interprété comme une langue et une page de codes indépendantes.</span><span class="sxs-lookup"><span data-stu-id="aac07-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="aac07-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aac07-137">Requirements</span></span>



| <span data-ttu-id="aac07-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aac07-138">Requirement</span></span> | <span data-ttu-id="aac07-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="aac07-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="aac07-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aac07-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aac07-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aac07-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aac07-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aac07-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aac07-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aac07-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="aac07-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aac07-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="aac07-145">**Référence**</span><span class="sxs-lookup"><span data-stu-id="aac07-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aac07-146">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="aac07-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="aac07-147">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="aac07-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="aac07-148">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="aac07-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="aac07-149">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="aac07-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="aac07-150">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="aac07-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aac07-151">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="aac07-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






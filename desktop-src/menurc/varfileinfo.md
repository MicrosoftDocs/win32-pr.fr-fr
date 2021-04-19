---
title: VarFileInfo, structure
description: Représente l’Organisation des données dans une ressource de version de fichier. Elle contient des informations sur la version qui ne dépendent pas d’une langue particulière et d’une combinaison de pages de codes.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menus de la structure VarFileInfo et autres ressources
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513810"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="fa898-105">VarFileInfo, structure</span><span class="sxs-lookup"><span data-stu-id="fa898-105">VarFileInfo structure</span></span>

<span data-ttu-id="fa898-106">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="fa898-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="fa898-107">Elle contient des informations sur la version qui ne dépendent pas d’une langue particulière et d’une combinaison de pages de codes.</span><span class="sxs-lookup"><span data-stu-id="fa898-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa898-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa898-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="fa898-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fa898-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa898-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="fa898-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="fa898-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-112">Longueur, en octets, du bloc **VarFileInfo** entier, y compris toutes les structures indiquées par le membre **Children** .</span><span class="sxs-lookup"><span data-stu-id="fa898-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="fa898-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="fa898-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-114">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="fa898-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-115">Ce membre est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fa898-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fa898-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="fa898-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-117">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="fa898-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-118">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="fa898-118">The type of data in the version resource.</span></span> <span data-ttu-id="fa898-119">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="fa898-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="fa898-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="fa898-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-121">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="fa898-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-122">Chaîne Unicode L "VarFileInfo".</span><span class="sxs-lookup"><span data-stu-id="fa898-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="fa898-123">**Remplissage**</span><span class="sxs-lookup"><span data-stu-id="fa898-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-124">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="fa898-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-125">Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fa898-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="fa898-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="fa898-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="fa898-127">Type : **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="fa898-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fa898-128">Contient généralement une liste de langues prises en charge par l’application ou la DLL.</span><span class="sxs-lookup"><span data-stu-id="fa898-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa898-129">Notes</span><span class="sxs-lookup"><span data-stu-id="fa898-129">Remarks</span></span>

<span data-ttu-id="fa898-130">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="fa898-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="fa898-131">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="fa898-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="fa898-132">Le membre **Children** de la structure de [**Visual Studio \_ VERSIONINFO**](vs-versioninfo.md) peut contenir zéro ou une structure **VarFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="fa898-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa898-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa898-133">Requirements</span></span>



| <span data-ttu-id="fa898-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa898-134">Requirement</span></span> | <span data-ttu-id="fa898-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa898-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fa898-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa898-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fa898-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa898-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fa898-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa898-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fa898-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa898-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fa898-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa898-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa898-141">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fa898-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa898-142">**Var**</span><span class="sxs-lookup"><span data-stu-id="fa898-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="fa898-143">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="fa898-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="fa898-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fa898-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fa898-145">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="fa898-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






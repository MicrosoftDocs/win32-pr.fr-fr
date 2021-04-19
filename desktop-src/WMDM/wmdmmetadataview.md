---
title: WMDMMetadataView, structure
description: La structure WMDMMetadataView définit la vue de métadonnées. Le contenu est organisé en fonction de cette définition.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Structure WMDMMetadataView Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527983"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="250f4-105">WMDMMetadataView, structure</span><span class="sxs-lookup"><span data-stu-id="250f4-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="250f4-106">La structure **WMDMMetadataView** définit la vue de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="250f4-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="250f4-107">Le contenu est organisé en fonction de cette définition.</span><span class="sxs-lookup"><span data-stu-id="250f4-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="250f4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="250f4-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="250f4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="250f4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="250f4-110">**pwszViewName**</span><span class="sxs-lookup"><span data-stu-id="250f4-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="250f4-111">Pointeur vers une chaîne de caractères larges se terminant par un caractère null qui contient le nom de la vue.</span><span class="sxs-lookup"><span data-stu-id="250f4-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="250f4-112">Il est utilisé comme nom du nœud racine sous lequel cette vue est présentée.</span><span class="sxs-lookup"><span data-stu-id="250f4-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="250f4-113">**nDepth**</span><span class="sxs-lookup"><span data-stu-id="250f4-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="250f4-114">Entier contenant la profondeur de la vue, qui indique le nombre de balises de métadonnées imbriquées utilisées pour la vue.</span><span class="sxs-lookup"><span data-stu-id="250f4-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="250f4-115">**ppwszTags**</span><span class="sxs-lookup"><span data-stu-id="250f4-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="250f4-116">Tableau de chaînes de balises de métadonnées pour les balises imbriquées.</span><span class="sxs-lookup"><span data-stu-id="250f4-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="250f4-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="250f4-117">Examples</span></span>

<span data-ttu-id="250f4-118">Le code suivant crée une vue de métadonnées :</span><span class="sxs-lookup"><span data-stu-id="250f4-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="250f4-119">Le code précédent organise le contenu comme suit :</span><span class="sxs-lookup"><span data-stu-id="250f4-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="250f4-120">Ma vue</span><span class="sxs-lookup"><span data-stu-id="250f4-120">My View</span></span><dl> <span data-ttu-id="250f4-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="250f4-121">Genre1</span></span><dl> <span data-ttu-id="250f4-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="250f4-122">Artist1</span></span><dl> <span data-ttu-id="250f4-123">Album1</span><span class="sxs-lookup"><span data-stu-id="250f4-123">Album1</span></span><dl> <span data-ttu-id="250f4-124">Song1</span><span class="sxs-lookup"><span data-stu-id="250f4-124">Song1</span></span>  
<span data-ttu-id="250f4-125">Song2</span><span class="sxs-lookup"><span data-stu-id="250f4-125">Song2</span></span>  
<span data-ttu-id="250f4-126">...</span><span class="sxs-lookup"><span data-stu-id="250f4-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="250f4-127">Album1</span><span class="sxs-lookup"><span data-stu-id="250f4-127">Album1</span></span><dl> <span data-ttu-id="250f4-128">Song1</span><span class="sxs-lookup"><span data-stu-id="250f4-128">Song1</span></span>  
<span data-ttu-id="250f4-129">Song2</span><span class="sxs-lookup"><span data-stu-id="250f4-129">Song2</span></span>  
<span data-ttu-id="250f4-130">...</span><span class="sxs-lookup"><span data-stu-id="250f4-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="250f4-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="250f4-131">Artist1</span></span><dl> <span data-ttu-id="250f4-132">Album1</span><span class="sxs-lookup"><span data-stu-id="250f4-132">Album1</span></span><dl> <span data-ttu-id="250f4-133">Song1</span><span class="sxs-lookup"><span data-stu-id="250f4-133">Song1</span></span>  
<span data-ttu-id="250f4-134">Song2</span><span class="sxs-lookup"><span data-stu-id="250f4-134">Song2</span></span>  
<span data-ttu-id="250f4-135">...</span><span class="sxs-lookup"><span data-stu-id="250f4-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="250f4-136">Album1</span><span class="sxs-lookup"><span data-stu-id="250f4-136">Album1</span></span><dl> <span data-ttu-id="250f4-137">Song1</span><span class="sxs-lookup"><span data-stu-id="250f4-137">Song1</span></span>  
<span data-ttu-id="250f4-138">Song2</span><span class="sxs-lookup"><span data-stu-id="250f4-138">Song2</span></span>  
<span data-ttu-id="250f4-139">...</span><span class="sxs-lookup"><span data-stu-id="250f4-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="250f4-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="250f4-140">Requirements</span></span>



| <span data-ttu-id="250f4-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="250f4-141">Requirement</span></span> | <span data-ttu-id="250f4-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="250f4-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="250f4-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="250f4-143">Header</span></span><br/> | <dl> <span data-ttu-id="250f4-144"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="250f4-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="250f4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="250f4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250f4-146">**Structures**</span><span class="sxs-lookup"><span data-stu-id="250f4-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






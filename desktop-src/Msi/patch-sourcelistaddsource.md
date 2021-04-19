---
description: La méthode SourceListAddSource ajoute un réseau ou une source d’URL. Accepte SourcePath, le type et l’index en tant que paramètres. Cette méthode appelle MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Méthode patch. SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543170"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="6d714-105">Méthode patch. SourceListAddSource</span><span class="sxs-lookup"><span data-stu-id="6d714-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="6d714-106">La méthode **SourceListAddSource** ajoute un réseau ou une source d’URL.</span><span class="sxs-lookup"><span data-stu-id="6d714-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="6d714-107">Accepte *SourcePath*, le *type* et l' *index* en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="6d714-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="6d714-108">Cette méthode appelle [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span><span class="sxs-lookup"><span data-stu-id="6d714-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d714-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d714-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="6d714-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d714-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d714-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="6d714-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="6d714-112">Type de source à ajouter : MSISOURCETYPE \_ réseau ou URL MSISOURCETYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="6d714-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="6d714-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="6d714-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="6d714-114">Chemin d’accès à la source à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6d714-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="6d714-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="6d714-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6d714-116">Si **SourceListAddSource** est appelé avec une nouvelle source et un nouvel *index* défini sur 0, le programme d’installation ajoute la source à la fin de la liste source.</span><span class="sxs-lookup"><span data-stu-id="6d714-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="6d714-117">Si cette fonction est appelée avec une source déjà existante dans la liste source et l' *index* a la valeur 0, le programme d’installation conserve l’index existant de la source.</span><span class="sxs-lookup"><span data-stu-id="6d714-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="6d714-118">Si la fonction est appelée avec une source existante dans la liste source et que l' *index* a une valeur différente de zéro, la source est supprimée de son emplacement actuel dans la liste et insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position.</span><span class="sxs-lookup"><span data-stu-id="6d714-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="6d714-119">Si la fonction est appelée avec une nouvelle source et que l' *index* est défini sur une valeur différente de zéro, la source est insérée à la position spécifiée par l' *index*, avant toute source qui existe déjà à cette position.</span><span class="sxs-lookup"><span data-stu-id="6d714-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="6d714-120">La valeur d’index pour toutes les sources de la liste après l’index spécifié par l' *index* est mise à jour pour garantir que les valeurs d’index uniques et la commande préexistante restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="6d714-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="6d714-121">Si l' *index* est supérieur au nombre de sources dans la liste, la source est placée à la fin de la liste avec une valeur d’index supérieure à une source existante.</span><span class="sxs-lookup"><span data-stu-id="6d714-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d714-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d714-122">Return value</span></span>

<span data-ttu-id="6d714-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6d714-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d714-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d714-124">Requirements</span></span>



| <span data-ttu-id="6d714-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d714-125">Requirement</span></span> | <span data-ttu-id="6d714-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d714-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d714-127">Version</span><span class="sxs-lookup"><span data-stu-id="6d714-127">Version</span></span><br/> | <span data-ttu-id="6d714-128">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d714-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6d714-129">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d714-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6d714-130">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6d714-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6d714-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6d714-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d714-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d714-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6d714-133">IID</span><span class="sxs-lookup"><span data-stu-id="6d714-133">IID</span></span><br/>     | <span data-ttu-id="6d714-134">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6d714-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="6d714-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d714-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d714-136">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="6d714-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="6d714-137">**MsiSourceListAddSourceEx**</span><span class="sxs-lookup"><span data-stu-id="6d714-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="6d714-138">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6d714-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





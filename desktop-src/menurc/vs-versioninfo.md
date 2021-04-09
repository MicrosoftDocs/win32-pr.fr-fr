---
title: Structure VS_VERSIONINFO
description: Représente l’Organisation des données dans une ressource de version de fichier. Il s’agit de la structure racine qui contient toutes les autres structures d’informations de version de fichier.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO des menus de structure et d’autres ressources
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106162"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="1c953-105">Structure de VS \_ VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="1c953-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="1c953-106">Représente l’Organisation des données dans une ressource de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="1c953-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="1c953-107">Il s’agit de la structure racine qui contient toutes les autres structures d’informations de version de fichier.</span><span class="sxs-lookup"><span data-stu-id="1c953-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c953-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c953-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="1c953-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1c953-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="1c953-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="1c953-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-112">Longueur, en octets, de la structure **vs \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="1c953-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="1c953-113">Cette longueur n’inclut aucun remplissage qui aligne les données de ressource de version suivantes sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1c953-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-114">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="1c953-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-115">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-116">Longueur, en octets, du membre de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="1c953-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="1c953-117">Cette valeur est égale à zéro si aucun membre de **valeur** n’est associé à la structure de la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="1c953-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="1c953-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-119">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-120">Type de données de la ressource de version.</span><span class="sxs-lookup"><span data-stu-id="1c953-120">The type of data in the version resource.</span></span> <span data-ttu-id="1c953-121">Ce membre est 1 si la ressource de version contient des données texte et 0 si la ressource de version contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="1c953-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="1c953-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-123">Type : **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="1c953-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-124">Chaîne Unicode L "info VS \_ version \_ ".</span><span class="sxs-lookup"><span data-stu-id="1c953-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="1c953-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="1c953-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-126">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-127">Contient autant de mots zéro que nécessaire pour aligner le membre **value** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1c953-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-128">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1c953-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-129">Type : **[ **vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="1c953-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-130">Données arbitraires associées à cette structure **Visual Studio \_ VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="1c953-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="1c953-131">Le membre **wValueLength** spécifie la longueur de ce membre ; Si **wValueLength** est égal à zéro, ce membre n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1c953-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="1c953-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-133">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-134">Autant de mots zéro que nécessaire pour aligner le membre **Children** sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1c953-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="1c953-135">Ces octets ne sont pas inclus dans **wValueLength**.</span><span class="sxs-lookup"><span data-stu-id="1c953-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="1c953-136">Ce membre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1c953-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="1c953-137">**Children**</span><span class="sxs-lookup"><span data-stu-id="1c953-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="1c953-138">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="1c953-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="1c953-139">Tableau de zéro ou une structure [**StringFileInfo**](stringfileinfo.md) , et zéro ou une structure [**VarFileInfo**](varfileinfo.md) qui sont des enfants de la structure **vs \_ VERSIONINFO** actuelle.</span><span class="sxs-lookup"><span data-stu-id="1c953-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c953-140">Notes</span><span class="sxs-lookup"><span data-stu-id="1c953-140">Remarks</span></span>

<span data-ttu-id="1c953-141">Cette structure n’est pas une véritable structure de langage C, car elle contient des membres de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="1c953-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="1c953-142">Cette structure a été créée uniquement pour représenter l’Organisation des données dans une ressource de version et n’apparaît pas dans les fichiers d’en-tête fournis avec le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="1c953-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c953-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c953-143">Requirements</span></span>



| <span data-ttu-id="1c953-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c953-144">Requirement</span></span> | <span data-ttu-id="1c953-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c953-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c953-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c953-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1c953-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c953-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c953-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c953-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1c953-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c953-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1c953-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c953-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c953-151">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1c953-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c953-152">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="1c953-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="1c953-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="1c953-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="1c953-154">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="1c953-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="1c953-155">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="1c953-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="1c953-156">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="1c953-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1c953-157">Informations sur la version</span><span class="sxs-lookup"><span data-stu-id="1c953-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 






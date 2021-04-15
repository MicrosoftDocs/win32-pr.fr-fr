---
title: ACCELTABLEENTRY, structure
description: Décrit les données dans une ressource de table d’accélérateurs individuelle. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Menus de la structure ACCELTABLEENTRY et autres ressources
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466886"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="c3d49-105">ACCELTABLEENTRY, structure</span><span class="sxs-lookup"><span data-stu-id="c3d49-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="c3d49-106">Décrit les données dans une ressource de table d’accélérateurs individuelle.</span><span class="sxs-lookup"><span data-stu-id="c3d49-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="c3d49-107">La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="c3d49-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d49-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3d49-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="c3d49-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c3d49-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3d49-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="c3d49-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c3d49-111">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="c3d49-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c3d49-112">Décrit les caractéristiques des accélérateurs clavier.</span><span class="sxs-lookup"><span data-stu-id="c3d49-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="c3d49-113">Ce membre peut avoir une ou plusieurs des valeurs suivantes de winuser. h.</span><span class="sxs-lookup"><span data-stu-id="c3d49-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="c3d49-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d49-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="c3d49-115">Signification</span><span class="sxs-lookup"><span data-stu-id="c3d49-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="c3d49-116"><dt>**FVIRTKEY**</dt> <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="c3d49-117">La touche accélérateur est un [Code de touche virtuelle](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="c3d49-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="c3d49-118">Si cet indicateur n’est pas spécifié, la touche d’accès rapide est supposée spécifier un code de caractère ASCII.</span><span class="sxs-lookup"><span data-stu-id="c3d49-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="c3d49-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="c3d49-120">Un élément de menu de la barre de menus n’est pas mis en surbrillance lorsqu’un accélérateur est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c3d49-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="c3d49-121">Cet attribut est obsolète et conservé uniquement à des fins de compatibilité descendante avec les fichiers de ressources conçus pour Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c3d49-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="c3d49-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="c3d49-123">L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="c3d49-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="c3d49-124">Cet indicateur s’applique uniquement aux clés virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c3d49-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="c3d49-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="c3d49-126">L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche CTRL.</span><span class="sxs-lookup"><span data-stu-id="c3d49-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="c3d49-127">Cet indicateur s’applique uniquement aux clés virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c3d49-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="c3d49-128"><dt>**Falt**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="c3d49-129">L’accélérateur est activé uniquement si l’utilisateur appuie sur la touche ALT.</span><span class="sxs-lookup"><span data-stu-id="c3d49-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="c3d49-130">Cet indicateur s’applique uniquement aux clés virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c3d49-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="c3d49-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="c3d49-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="c3d49-132">L’entrée est la dernière dans une table d’accélérateurs.</span><span class="sxs-lookup"><span data-stu-id="c3d49-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="c3d49-133">**wAnsi**</span><span class="sxs-lookup"><span data-stu-id="c3d49-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="c3d49-134">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="c3d49-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c3d49-135">Valeur de caractère ANSI ou code de touche virtuelle qui identifie la touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="c3d49-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="c3d49-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="c3d49-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="c3d49-137">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="c3d49-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c3d49-138">Identificateur de l’accélérateur clavier.</span><span class="sxs-lookup"><span data-stu-id="c3d49-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="c3d49-139">Il s’agit de la valeur passée à la procédure de fenêtre lorsque l’utilisateur appuie sur la touche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3d49-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="c3d49-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="c3d49-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="c3d49-141">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="c3d49-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c3d49-142">Nombre d’octets insérés pour garantir que la structure est alignée sur une limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c3d49-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3d49-143">Notes</span><span class="sxs-lookup"><span data-stu-id="c3d49-143">Remarks</span></span>

<span data-ttu-id="c3d49-144">La structure **ACCELTABLEENTRY** est répétée pour toutes les entrées de la table d’accélérateurs dans la ressource.</span><span class="sxs-lookup"><span data-stu-id="c3d49-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="c3d49-145">La dernière entrée de la table est marquée avec la valeur 0x0080.</span><span class="sxs-lookup"><span data-stu-id="c3d49-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="c3d49-146">Vous pouvez calculer le nombre d’éléments dans la table si vous divisez la longueur de la ressource par huit.</span><span class="sxs-lookup"><span data-stu-id="c3d49-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="c3d49-147">Ensuite, votre application peut accéder de manière aléatoire aux entrées de longueur fixe individuelles.</span><span class="sxs-lookup"><span data-stu-id="c3d49-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d49-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d49-148">Requirements</span></span>



| <span data-ttu-id="c3d49-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d49-149">Requirement</span></span> | <span data-ttu-id="c3d49-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d49-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3d49-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d49-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d49-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3d49-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3d49-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d49-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d49-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3d49-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3d49-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3d49-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3d49-156">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c3d49-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3d49-157">**CreateAcceleratorTable**</span><span class="sxs-lookup"><span data-stu-id="c3d49-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="c3d49-158">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c3d49-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c3d49-159">Ressources</span><span class="sxs-lookup"><span data-stu-id="c3d49-159">Resources</span></span>](resources.md)
</dt> </dl>

 


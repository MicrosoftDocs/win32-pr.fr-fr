---
description: Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: DEVICEDIALOGDATA, structure (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529157"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="7dc32-103">DEVICEDIALOGDATA, structure</span><span class="sxs-lookup"><span data-stu-id="7dc32-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="7dc32-104">Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7dc32-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dc32-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="7dc32-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7dc32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dc32-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7dc32-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7dc32-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-109">Spécifie la taille de cette structure en octets.</span><span class="sxs-lookup"><span data-stu-id="7dc32-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7dc32-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="7dc32-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-111">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="7dc32-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-112">Spécifie le handle vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7dc32-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="7dc32-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="7dc32-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-114">Tapez : \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="7dc32-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-115">Pointe vers une interface [_ *IWiaItem* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) qui représente l’élément racine valide dans l’arborescence d’éléments de l’application.</span><span class="sxs-lookup"><span data-stu-id="7dc32-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="7dc32-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="7dc32-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-117">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7dc32-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-118">Spécifie un jeu d’indicateurs qui contrôlent l’opération de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7dc32-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="7dc32-119">Peut être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7dc32-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="7dc32-120">Indicateur</span><span class="sxs-lookup"><span data-stu-id="7dc32-120">Flag</span></span>                                 | <span data-ttu-id="7dc32-121">Signification</span><span class="sxs-lookup"><span data-stu-id="7dc32-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc32-122">0</span><span class="sxs-lookup"><span data-stu-id="7dc32-122">0</span></span>                                    | <span data-ttu-id="7dc32-123">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="7dc32-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="7dc32-124">IMAGE unique de la boîte de dialogue de l' \_ appareil WIA \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7dc32-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="7dc32-125">Limitez la sélection d’image à une seule image dans la boîte de dialogue acquisition d’image d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7dc32-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="7dc32-126">\_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune</span><span class="sxs-lookup"><span data-stu-id="7dc32-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="7dc32-127">Utilisez l’interface utilisateur du système, si elle est disponible, au lieu de l’interface utilisateur fournie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7dc32-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="7dc32-128">Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7dc32-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="7dc32-129">Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="7dc32-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7dc32-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="7dc32-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-131">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="7dc32-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-132">Spécifie le type de données que l’image doit représenter.</span><span class="sxs-lookup"><span data-stu-id="7dc32-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="7dc32-133">Pour obtenir la liste des valeurs d’intention d’image, consultez [**constantes d’intention d’image**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="7dc32-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7dc32-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="7dc32-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-135">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="7dc32-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-136">Reçoit le nombre d’éléments dans le tableau indiqué par le paramètre **ppWiaItem** .</span><span class="sxs-lookup"><span data-stu-id="7dc32-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7dc32-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="7dc32-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="7dc32-138">Type : **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="7dc32-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="7dc32-139">Reçoit l’adresse d’un tableau de pointeurs vers des interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="7dc32-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dc32-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dc32-140">Requirements</span></span>



| <span data-ttu-id="7dc32-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dc32-141">Requirement</span></span> | <span data-ttu-id="7dc32-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dc32-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc32-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc32-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc32-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc32-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7dc32-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc32-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc32-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc32-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7dc32-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dc32-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc32-148"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc32-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 





---
title: ImageList_SetColorTable fonction)
description: Définit la table des couleurs pour une liste d’images.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- Contrôles Windows de la fonction ImageList_SetColorTable
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942928"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="9230a-104">\_Fonction SetColorTable ImageList</span><span class="sxs-lookup"><span data-stu-id="9230a-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="9230a-105">Définit la table des couleurs pour une liste d’images.</span><span class="sxs-lookup"><span data-stu-id="9230a-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9230a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9230a-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="9230a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9230a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9230a-108">*himl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230a-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230a-109">Type : **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="9230a-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="9230a-110">Handle de la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="9230a-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="9230a-111">*Démarrer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230a-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230a-112">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="9230a-112">Type: **int**</span></span>

<span data-ttu-id="9230a-113">Index de table de couleur de base zéro qui spécifie la première entrée de la table des couleurs à définir.</span><span class="sxs-lookup"><span data-stu-id="9230a-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="9230a-114">*Len* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230a-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230a-115">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="9230a-115">Type: **int**</span></span>

<span data-ttu-id="9230a-116">Nombre d’entrées de table des couleurs à définir.</span><span class="sxs-lookup"><span data-stu-id="9230a-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="9230a-117">*prgb* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9230a-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9230a-118">Tapez : \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="9230a-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="9230a-119">Pointeur vers un tableau de structures _len \* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) contenant de nouvelles informations de couleur pour la table des couleurs du dib.</span><span class="sxs-lookup"><span data-stu-id="9230a-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9230a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9230a-120">Return value</span></span>

<span data-ttu-id="9230a-121">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="9230a-121">Type: **int**</span></span>

<span data-ttu-id="9230a-122">Si la fonction est réussie, elle retourne le nombre d’entrées de table des couleurs définies par la fonction.</span><span class="sxs-lookup"><span data-stu-id="9230a-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="9230a-123">Si la fonction échoue, la valeur de retour est inférieure ou égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="9230a-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9230a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9230a-124">Remarks</span></span>

<span data-ttu-id="9230a-125">Seules les listes d’images créées avec l’indicateur [**ILC \_ color4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ou [**ILC \_ color8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ont des tables de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9230a-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="9230a-126">La table des couleurs d’une telle liste d’images est généralement définie automatiquement en copiant la table des couleurs de la première image ajoutée à la liste (par exemple, à l’aide de la fonction [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) si cette image est un dib.</span><span class="sxs-lookup"><span data-stu-id="9230a-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="9230a-127">Si la première image ajoutée à la liste d’images n’est pas un DIB, la table des couleurs de la palette de demi-teintes est utilisée pour les listes d’images **ILC \_ color8** et la table de couleurs VGA est utilisée pour **ILC \_ color4**.</span><span class="sxs-lookup"><span data-stu-id="9230a-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9230a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9230a-128">Requirements</span></span>



| <span data-ttu-id="9230a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9230a-129">Requirement</span></span> | <span data-ttu-id="9230a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9230a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9230a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9230a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9230a-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9230a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="9230a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9230a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9230a-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9230a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9230a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9230a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9230a-136"><dt>Comctl32.dll (version 3,51 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9230a-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9230a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9230a-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="9230a-138">[Table des couleurs](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="9230a-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 


---
title: Structure DSA_SEC_PAGE_INFO
description: Utilisé avec la feuille de calcul WM \_ ADSPROP \_ et la \_ \_ feuille DSA, \_ créer des \_ \_ messages de notification pour définir une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO structure Active Directory
- Pointeur de structure PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942392"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="46627-105">Structure des informations de la \_ page DSA sec \_ \_</span><span class="sxs-lookup"><span data-stu-id="46627-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="46627-106">La structure des informations de la **\_ \_ page \_ DSA s** est utilisée avec les feuilles de propriétés [**WM \_ ADSPROP \_ \_**](wm-adsprop-sheet-create.md) et [**WM \_ DSA \_ \_ créer \_**](wm-dsa-sheet-create-notify.md) des messages Notify pour définir une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46627-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="46627-107">Cette structure n’est pas définie dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="46627-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="46627-108">Pour utiliser cette structure, définissez-la dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="46627-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="46627-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46627-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="46627-110">Membres</span><span class="sxs-lookup"><span data-stu-id="46627-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="46627-111">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="46627-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="46627-112">Contient le handle de fenêtre du parent de la feuille de propriétés secondaire.</span><span class="sxs-lookup"><span data-stu-id="46627-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="46627-113">**offsetTitle**</span><span class="sxs-lookup"><span data-stu-id="46627-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="46627-114">Contient l’offset, en octets, entre le début de la structure des informations de la **\_ \_ page \_ DSA s** et une chaîne Unicode terminée par le caractère null qui contient le titre de la feuille de propriétés secondaire.</span><span class="sxs-lookup"><span data-stu-id="46627-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="46627-115">**dsObjectNames**</span><span class="sxs-lookup"><span data-stu-id="46627-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="46627-116">Contient une structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) qui définit la feuille de propriétés secondaire.</span><span class="sxs-lookup"><span data-stu-id="46627-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="46627-117">Une seule feuille de propriétés secondaire peut être créée à la fois, de sorte que la structure **DSOBJECTNAMES** ne peut contenir qu’une seule structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="46627-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46627-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46627-118">Requirements</span></span>



| <span data-ttu-id="46627-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46627-119">Requirement</span></span> | <span data-ttu-id="46627-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="46627-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="46627-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46627-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46627-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46627-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="46627-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46627-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46627-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46627-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46627-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46627-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46627-126">**création de la \_ feuille ADSPROP WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46627-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="46627-127">**créer une notification de la \_ feuille DSA DSA \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="46627-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="46627-128">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="46627-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="46627-129">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="46627-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 






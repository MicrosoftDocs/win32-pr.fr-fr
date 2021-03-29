---
description: SFVM \_ GETDETAILSOF peut être modifié ou non disponible.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Message SFVM_GETDETAILSOF (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973482"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="e61fa-103">\_Message SFVM GETDETAILSOF</span><span class="sxs-lookup"><span data-stu-id="e61fa-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="e61fa-104">\[**SFVM \_ GETDETAILSOF** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e61fa-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e61fa-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="e61fa-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e61fa-106">Permet à l’objet de rappel de fournir les détails d’un élément dans un dossier de Shell.</span><span class="sxs-lookup"><span data-stu-id="e61fa-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="e61fa-107">À utiliser uniquement si un appel à [**IShellFolder2 :: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) échoue et qu’il n’existe aucune méthode [**IShellDetails :: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponible pour appeler.</span><span class="sxs-lookup"><span data-stu-id="e61fa-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="e61fa-108">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e61fa-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="e61fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e61fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61fa-110">*IColumn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e61fa-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e61fa-111">ID de base zéro de la colonne.</span><span class="sxs-lookup"><span data-stu-id="e61fa-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="e61fa-112">*pDi* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e61fa-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e61fa-113">Pointeur vers une structure [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) remplie avec les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="e61fa-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e61fa-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e61fa-114">Requirements</span></span>



| <span data-ttu-id="e61fa-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e61fa-115">Requirement</span></span> | <span data-ttu-id="e61fa-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e61fa-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e61fa-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e61fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e61fa-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e61fa-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e61fa-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e61fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e61fa-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e61fa-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e61fa-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e61fa-121">End of client support</span></span><br/>    | <span data-ttu-id="e61fa-122">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="e61fa-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="e61fa-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e61fa-123">End of server support</span></span><br/>    | <span data-ttu-id="e61fa-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e61fa-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="e61fa-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e61fa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61fa-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61fa-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

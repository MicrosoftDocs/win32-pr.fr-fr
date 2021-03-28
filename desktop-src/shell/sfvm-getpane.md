---
description: SFVM \_ GETPANE peut être modifié ou non disponible.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Message SFVM_GETPANE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952334"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="8aee7-103">\_Message SFVM GETPANE</span><span class="sxs-lookup"><span data-stu-id="8aee7-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="8aee7-104">\[**SFVM \_ GETPANE** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8aee7-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8aee7-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="8aee7-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="8aee7-106">Permet à l’objet de rappel de fournir le volet de barre d’État dans lequel afficher les informations de la zone Internet.</span><span class="sxs-lookup"><span data-stu-id="8aee7-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="8aee7-107">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8aee7-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="8aee7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8aee7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aee7-109">*paneID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8aee7-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8aee7-110">ID du volet demandé.</span><span class="sxs-lookup"><span data-stu-id="8aee7-110">ID of the requested pane.</span></span> <span data-ttu-id="8aee7-111">Il s’agit normalement \_ de la zone de volet, mais peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8aee7-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="8aee7-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**VOLET \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="8aee7-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-113">Aucun volet.</span><span class="sxs-lookup"><span data-stu-id="8aee7-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="8aee7-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**ZONE de volet \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-115">Volet zone Internet.</span><span class="sxs-lookup"><span data-stu-id="8aee7-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="8aee7-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**VOLET \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="8aee7-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-117">Volet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8aee7-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="8aee7-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**imprimante du volet \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-119">Le volet d’indication d’impression.</span><span class="sxs-lookup"><span data-stu-id="8aee7-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="8aee7-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL de volet \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-121">Le volet SSL.</span><span class="sxs-lookup"><span data-stu-id="8aee7-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="8aee7-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**NAVIGATION dans les VOLETs \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-123">Volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="8aee7-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="8aee7-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progression du volet \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-125">Volet de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="8aee7-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="8aee7-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**confidentialité du volet \_**</span><span class="sxs-lookup"><span data-stu-id="8aee7-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="8aee7-127">Volet de l’indicateur de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="8aee7-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8aee7-128">*volet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8aee7-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8aee7-129">Pointeur vers une **valeur DWORD** contenant le numéro du volet.</span><span class="sxs-lookup"><span data-stu-id="8aee7-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8aee7-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8aee7-130">Requirements</span></span>



| <span data-ttu-id="8aee7-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8aee7-131">Requirement</span></span> | <span data-ttu-id="8aee7-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8aee7-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8aee7-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8aee7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8aee7-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8aee7-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8aee7-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8aee7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8aee7-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8aee7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8aee7-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8aee7-137">End of client support</span></span><br/>    | <span data-ttu-id="8aee7-138">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="8aee7-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="8aee7-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8aee7-139">End of server support</span></span><br/>    | <span data-ttu-id="8aee7-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8aee7-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="8aee7-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="8aee7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aee7-142"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aee7-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

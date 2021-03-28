---
description: 'Permet à l’objet de rappel d’ajouter des boutons à la barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETBUTTONINFO (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973486"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="d7418-104">\_Message SFVM GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="d7418-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="d7418-105">Permet à l’objet de rappel d’ajouter des boutons à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d7418-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="d7418-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d7418-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="d7418-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7418-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7418-108">*ptbinfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7418-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7418-109">Adresse d’une structure [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) qui spécifie le nombre de boutons et la façon dont ils doivent être ajoutés à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d7418-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7418-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d7418-110">Remarks</span></span>

<span data-ttu-id="d7418-111">Les boutons peuvent être ajoutés aux boutons de l’objet d’affichage des dossiers système standard ou être ajoutés à la place des boutons standard.</span><span class="sxs-lookup"><span data-stu-id="d7418-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="d7418-112">Ce message est suivi d’un message [**SFVM \_ GETBUTTONS**](sfvm-getbuttons.md) qui extrait les informations relatives aux spécificités du bouton.</span><span class="sxs-lookup"><span data-stu-id="d7418-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7418-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7418-113">Requirements</span></span>



| <span data-ttu-id="d7418-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7418-114">Requirement</span></span> | <span data-ttu-id="d7418-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7418-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7418-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7418-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7418-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7418-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7418-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7418-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7418-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7418-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7418-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7418-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7418-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7418-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

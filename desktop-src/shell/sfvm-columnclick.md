---
description: 'Notifie l’objet de rappel sur lequel l’utilisateur a cliqué sur un en-tête de colonne pour trier la liste d’objets dans l’affichage des dossiers. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_COLUMNCLICK (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485513"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="6e671-104">\_Message SFVM COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="6e671-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="6e671-105">Notifie l’objet de rappel sur lequel l’utilisateur a cliqué sur un en-tête de colonne pour trier la liste d’objets dans l’affichage des dossiers.</span><span class="sxs-lookup"><span data-stu-id="6e671-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="6e671-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6e671-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="6e671-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e671-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e671-108">*IColumn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6e671-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e671-109">Index de la colonne sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="6e671-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e671-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6e671-110">Remarks</span></span>

<span data-ttu-id="6e671-111">En réponse à cette notification, vous devez retourner S \_ OK pour réorganiser la liste vous-même.</span><span class="sxs-lookup"><span data-stu-id="6e671-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="6e671-112">Pour que l’objet de vue de dossier système réorganise la liste, retourne la \_ valeur false.</span><span class="sxs-lookup"><span data-stu-id="6e671-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e671-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6e671-113">Requirements</span></span>



| <span data-ttu-id="6e671-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e671-114">Requirement</span></span> | <span data-ttu-id="6e671-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e671-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e671-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e671-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e671-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e671-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6e671-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e671-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e671-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e671-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e671-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e671-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e671-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e671-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 

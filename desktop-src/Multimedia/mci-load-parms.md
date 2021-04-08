---
title: Structure de MCI_LOAD_PARMS (mmsystem. h)
description: La \_ \_ structure des PARMS de chargement MCI contient le nom de fichier à charger pour la \_ commande de chargement MCI.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Structure de MCI_LOAD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742948"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="2fd4a-104">Structure des PARMS de \_ chargement MCI \_</span><span class="sxs-lookup"><span data-stu-id="2fd4a-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="2fd4a-105">La structure des **\_ \_ PARMS de chargement MCI** contient le nom de fichier à charger pour la commande de [**\_ chargement MCI**](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="2fd4a-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd4a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fd4a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="2fd4a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2fd4a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2fd4a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2fd4a-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2fd4a-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="2fd4a-111">Nom du fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fd4a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2fd4a-112">Remarks</span></span>

<span data-ttu-id="2fd4a-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="2fd4a-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd4a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fd4a-114">Requirements</span></span>



| <span data-ttu-id="2fd4a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fd4a-115">Requirement</span></span> | <span data-ttu-id="2fd4a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fd4a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd4a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fd4a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd4a-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fd4a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2fd4a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fd4a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd4a-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fd4a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fd4a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fd4a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fd4a-122"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fd4a-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd4a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fd4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd4a-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2fd4a-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2fd4a-126">**\_chargement MCI**</span><span class="sxs-lookup"><span data-stu-id="2fd4a-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="2fd4a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2fd4a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


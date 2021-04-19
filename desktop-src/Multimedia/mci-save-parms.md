---
title: Structure MCI_SAVE_PARMS (Mciapi. h)
description: La \_ structure MCI Save \_ PARMS contient les informations de nom de fichier pour la \_ commande d’enregistrement MCI.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- Structure de MCI_SAVE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509904"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="338ef-104">\_Enregistrer la \_ structure des PARMS avec MCI</span><span class="sxs-lookup"><span data-stu-id="338ef-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="338ef-105">La structure **MCI \_ Save \_ PARMS** contient les informations de nom de fichier pour la commande d' [**\_ enregistrement MCI**](mci-save.md) .</span><span class="sxs-lookup"><span data-stu-id="338ef-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="338ef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="338ef-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="338ef-107">Membres</span><span class="sxs-lookup"><span data-stu-id="338ef-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="338ef-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="338ef-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="338ef-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="338ef-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="338ef-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="338ef-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="338ef-111">Nom du fichier à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="338ef-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="338ef-112">Notes</span><span class="sxs-lookup"><span data-stu-id="338ef-112">Remarks</span></span>

<span data-ttu-id="338ef-113">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="338ef-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="338ef-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="338ef-114">Requirements</span></span>



| <span data-ttu-id="338ef-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="338ef-115">Requirement</span></span> | <span data-ttu-id="338ef-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="338ef-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="338ef-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="338ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="338ef-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="338ef-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="338ef-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="338ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="338ef-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="338ef-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="338ef-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="338ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="338ef-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="338ef-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338ef-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="338ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338ef-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="338ef-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="338ef-125">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="338ef-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="338ef-126">**\_enregistrement MCI**</span><span class="sxs-lookup"><span data-stu-id="338ef-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="338ef-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="338ef-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


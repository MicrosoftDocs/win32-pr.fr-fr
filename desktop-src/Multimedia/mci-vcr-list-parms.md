---
title: Structure de MCI_VCR_LIST_PARMS (VCR. h)
description: La structure de la \_ liste des magnétoscopes MCI \_ contient des \_ paramètres pour la \_ commande de liste MCI pour les enregistreurs de cassettes vidéo.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- Structure de MCI_VCR_LIST_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317438"
---
# <a name="mci_vcr_list_parms-structure"></a><span data-ttu-id="1743d-104">\_Liste des magnétoscopes MCI \_ \_ structure PARMS</span><span class="sxs-lookup"><span data-stu-id="1743d-104">MCI\_VCR\_LIST\_PARMS structure</span></span>

<span data-ttu-id="1743d-105">La structure de la **\_ \_ liste \_ des magnétoscopes MCI** contient des paramètres pour la commande de [**\_ liste MCI**](mci-list.md) pour les enregistreurs de cassettes vidéo.</span><span class="sxs-lookup"><span data-stu-id="1743d-105">The **MCI\_VCR\_LIST\_PARMS** structure contains parameters for the [**MCI\_LIST**](mci-list.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="1743d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1743d-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a><span data-ttu-id="1743d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="1743d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1743d-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="1743d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1743d-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="1743d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1743d-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="1743d-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="1743d-111">Mémoire tampon pour les informations renvoyées.</span><span class="sxs-lookup"><span data-stu-id="1743d-111">Buffer for returned information.</span></span>

</dd> <dt>

<span data-ttu-id="1743d-112">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="1743d-112">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1743d-113">Nombre d’entrées vidéo ou audio du magnétoscope.</span><span class="sxs-lookup"><span data-stu-id="1743d-113">Number of VCR's video or audio inputs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1743d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1743d-114">Remarks</span></span>

<span data-ttu-id="1743d-115">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="1743d-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1743d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1743d-116">Requirements</span></span>



| <span data-ttu-id="1743d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1743d-117">Requirement</span></span> | <span data-ttu-id="1743d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1743d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1743d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1743d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1743d-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1743d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1743d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1743d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1743d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1743d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1743d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1743d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1743d-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="1743d-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1743d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1743d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1743d-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1743d-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1743d-127">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="1743d-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1743d-128">**\_liste MCI**</span><span class="sxs-lookup"><span data-stu-id="1743d-128">**MCI\_LIST**</span></span>](mci-list.md)
</dt> <dt>

<span data-ttu-id="1743d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1743d-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


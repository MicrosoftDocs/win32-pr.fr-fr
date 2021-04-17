---
title: Structure de MCI_VCR_SEEK_PARMS (VCR. h)
description: La structure de la \_ recherche MCI VCR \_ contient des \_ paramètres pour la \_ commande MCI Seek pour les enregistreurs vidéo-cassettes.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Structure de MCI_VCR_SEEK_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464834"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="2520f-104">Structure de la \_ recherche MCI VCR \_ \_</span><span class="sxs-lookup"><span data-stu-id="2520f-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="2520f-105">La structure de la **\_ \_ \_ recherche MCI VCR** contient des paramètres pour la commande [**MCI \_ Seek**](mci-seek.md) pour les enregistreurs vidéo-cassettes.</span><span class="sxs-lookup"><span data-stu-id="2520f-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="2520f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2520f-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="2520f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2520f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2520f-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="2520f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2520f-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="2520f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2520f-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="2520f-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="2520f-111">Position à laquelle effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="2520f-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="2520f-112">**dwMark**</span><span class="sxs-lookup"><span data-stu-id="2520f-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="2520f-113">Marque numérotée à rechercher.</span><span class="sxs-lookup"><span data-stu-id="2520f-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="2520f-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="2520f-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="2520f-115">Heure de début de la recherche.</span><span class="sxs-lookup"><span data-stu-id="2520f-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2520f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2520f-116">Remarks</span></span>

<span data-ttu-id="2520f-117">Les positions sont spécifiées dans le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="2520f-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="2520f-118">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="2520f-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2520f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2520f-119">Requirements</span></span>



| <span data-ttu-id="2520f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2520f-120">Requirement</span></span> | <span data-ttu-id="2520f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2520f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2520f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2520f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2520f-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2520f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2520f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2520f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2520f-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2520f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2520f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2520f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2520f-127"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="2520f-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2520f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2520f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2520f-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2520f-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2520f-130">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="2520f-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2520f-131">**\_recherche MCI**</span><span class="sxs-lookup"><span data-stu-id="2520f-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="2520f-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2520f-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


---
title: Structure de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ structure MCI OVLY \_ Open \_ PARMS contient des informations pour la \_ commande MCI Open pour les périphériques de superposition vidéo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Structure de MCI_OVLY_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464227"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="4167a-104">\_OVLY \_ Open \_ PARMS, MCI</span><span class="sxs-lookup"><span data-stu-id="4167a-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="4167a-105">La structure **MCI \_ OVLY \_ Open \_ PARMS** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) pour les périphériques de superposition vidéo.</span><span class="sxs-lookup"><span data-stu-id="4167a-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4167a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4167a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="4167a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4167a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4167a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="4167a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="4167a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="4167a-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4167a-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-111">Identificateur retourné à l’application.</span><span class="sxs-lookup"><span data-stu-id="4167a-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="4167a-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="4167a-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-113">Nom ou identificateur de constante du type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4167a-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="4167a-114">(Le nom de l’appareil est généralement obtenu à partir du registre ou du fichier SYSTEM.INI.) Si ce membre est une constante, il peut s’agir de l’une des valeurs indiquées dans [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="4167a-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="4167a-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="4167a-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-116">Nom de l’élément d’appareil (généralement un chemin d’accès).</span><span class="sxs-lookup"><span data-stu-id="4167a-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="4167a-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="4167a-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-118">Alias d’appareil facultatif.</span><span class="sxs-lookup"><span data-stu-id="4167a-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="4167a-119">**dwStyle**</span><span class="sxs-lookup"><span data-stu-id="4167a-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-120">Style de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4167a-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="4167a-121">**hWndParent**</span><span class="sxs-lookup"><span data-stu-id="4167a-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="4167a-122">Handle vers la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="4167a-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4167a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4167a-123">Remarks</span></span>

<span data-ttu-id="4167a-124">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="4167a-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="4167a-125">Vous pouvez utiliser la [**structure \_ Open \_ parmss MCI**](mci-open-parms.md) à la place de **MCI \_ OVLY \_ ouvrir \_ parms** si vous n’utilisez pas les membres de données étendus.</span><span class="sxs-lookup"><span data-stu-id="4167a-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="4167a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4167a-126">Requirements</span></span>



| <span data-ttu-id="4167a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4167a-127">Requirement</span></span> | <span data-ttu-id="4167a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4167a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4167a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4167a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4167a-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4167a-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4167a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4167a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4167a-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4167a-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4167a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="4167a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4167a-134"><dt>MMSYSTEM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4167a-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4167a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4167a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4167a-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4167a-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4167a-137">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="4167a-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="4167a-138">**MCI \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="4167a-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="4167a-139">**les \_ PARMS ouverts MCI \_**</span><span class="sxs-lookup"><span data-stu-id="4167a-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="4167a-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4167a-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


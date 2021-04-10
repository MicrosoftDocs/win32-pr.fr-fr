---
title: Structure MCI_OPEN_PARMS (Mciapi. h)
description: La \_ structure MCI Open \_ PARMS contient des informations pour la \_ commande MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- Structure de MCI_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103441"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="cebcd-104">\_Structure d’ouverture des \_ PARMS MCI</span><span class="sxs-lookup"><span data-stu-id="cebcd-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="cebcd-105">La structure **MCI \_ Open \_ PARMS** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="cebcd-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="cebcd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cebcd-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="cebcd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cebcd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cebcd-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="cebcd-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="cebcd-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="cebcd-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="cebcd-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cebcd-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="cebcd-111">Identificateur retourné à l’application.</span><span class="sxs-lookup"><span data-stu-id="cebcd-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="cebcd-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="cebcd-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="cebcd-113">Nom ou identificateur de constante du type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="cebcd-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="cebcd-114">(Le nom de l’appareil est généralement obtenu à partir du registre ou du fichier SYSTEM.INI.) Si ce membre est une constante, il peut s’agir de l’une des valeurs indiquées dans [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="cebcd-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="cebcd-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="cebcd-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="cebcd-116">Élément d’appareil (souvent un chemin d’accès).</span><span class="sxs-lookup"><span data-stu-id="cebcd-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="cebcd-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="cebcd-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="cebcd-118">Alias d’appareil facultatif.</span><span class="sxs-lookup"><span data-stu-id="cebcd-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cebcd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="cebcd-119">Remarks</span></span>

<span data-ttu-id="cebcd-120">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="cebcd-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebcd-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cebcd-121">Requirements</span></span>



| <span data-ttu-id="cebcd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cebcd-122">Requirement</span></span> | <span data-ttu-id="cebcd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebcd-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cebcd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cebcd-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cebcd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cebcd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cebcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cebcd-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cebcd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cebcd-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cebcd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cebcd-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cebcd-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebcd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cebcd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cebcd-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="cebcd-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="cebcd-132">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="cebcd-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="cebcd-133">**MCI \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="cebcd-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="cebcd-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cebcd-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


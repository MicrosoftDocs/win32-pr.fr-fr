---
title: Structure MCI_SYSINFO_PARMS (Mciapi. h)
description: La \_ \_ structure de l’option MCI sysinfo PARMS contient des informations pour la \_ commande MCI sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Structure de MCI_SYSINFO_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513576"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="c26a0-104">\_Structure des \_ PARMS MCI sysinfo</span><span class="sxs-lookup"><span data-stu-id="c26a0-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="c26a0-105">La structure de l’option **MCI \_ sysinfo \_ PARMS** contient des informations pour la commande [**MCI \_ sysinfo**](mci-sysinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c26a0-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c26a0-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="c26a0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c26a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c26a0-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c26a0-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c26a0-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="c26a0-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c26a0-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="c26a0-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="c26a0-111">Pointeur vers une mémoire tampon fournie par l’utilisateur pour la chaîne de retour.</span><span class="sxs-lookup"><span data-stu-id="c26a0-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="c26a0-112">Elle est également utilisée pour retourner une valeur **DWORD** lorsque l' \_ indicateur de quantité MCI sysinfo \_ est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c26a0-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="c26a0-113">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="c26a0-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="c26a0-114">Taille, en octets, de la mémoire tampon de retour.</span><span class="sxs-lookup"><span data-stu-id="c26a0-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c26a0-115">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="c26a0-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c26a0-116">Nombre indiquant la position de l’appareil dans la table du périphérique MCI ou dans la liste des appareils ouverts si l' \_ indicateur d’ouverture MCI sysinfo \_ est défini.</span><span class="sxs-lookup"><span data-stu-id="c26a0-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="c26a0-117">**wDeviceType**</span><span class="sxs-lookup"><span data-stu-id="c26a0-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="c26a0-118">Type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c26a0-118">Type of device.</span></span> <span data-ttu-id="c26a0-119">Ce membre peut être l’une des valeurs indiquées dans les [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="c26a0-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c26a0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c26a0-120">Remarks</span></span>

<span data-ttu-id="c26a0-121">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="c26a0-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26a0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c26a0-122">Requirements</span></span>



| <span data-ttu-id="c26a0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c26a0-123">Requirement</span></span> | <span data-ttu-id="c26a0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c26a0-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c26a0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c26a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c26a0-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c26a0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c26a0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c26a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c26a0-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c26a0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c26a0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c26a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c26a0-130"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c26a0-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c26a0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c26a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26a0-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c26a0-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c26a0-133">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="c26a0-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c26a0-134">**MCI \_ sysinfo**</span><span class="sxs-lookup"><span data-stu-id="c26a0-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="c26a0-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c26a0-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


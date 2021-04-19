---
title: Structure MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: La \_ structure des \_ fonctions Open PARMS de l’onde MCI \_ contient des informations pour la \_ commande MCI Open pour les périphériques audio Waveform.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Structure de MCI_WAVE_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510155"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="24a1d-104">\_Structure des \_ PARMS d’ouverture MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="24a1d-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="24a1d-105">La structure des fonctions **\_ \_ Open \_ PARMS de l’onde MCI** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) pour les périphériques audio Waveform.</span><span class="sxs-lookup"><span data-stu-id="24a1d-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a1d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24a1d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="24a1d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="24a1d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="24a1d-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="24a1d-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-109">Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.</span><span class="sxs-lookup"><span data-stu-id="24a1d-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="24a1d-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="24a1d-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-111">Identificateur renvoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="24a1d-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="24a1d-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="24a1d-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-113">Nom ou identificateur de constante du type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="24a1d-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="24a1d-114">(Le nom de l’appareil est généralement obtenu à partir du registre ou du fichier SYSTEM.INI.) Ce membre peut être l’une des valeurs indiquées dans les [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="24a1d-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="24a1d-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="24a1d-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-116">Nom de l’élément d’appareil (généralement un chemin d’accès).</span><span class="sxs-lookup"><span data-stu-id="24a1d-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="24a1d-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="24a1d-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-118">Alias d’appareil facultatif.</span><span class="sxs-lookup"><span data-stu-id="24a1d-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="24a1d-119">**dwBufferSeconds**</span><span class="sxs-lookup"><span data-stu-id="24a1d-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="24a1d-120">Longueur de la mémoire tampon, en secondes.</span><span class="sxs-lookup"><span data-stu-id="24a1d-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24a1d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="24a1d-121">Remarks</span></span>

<span data-ttu-id="24a1d-122">Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.</span><span class="sxs-lookup"><span data-stu-id="24a1d-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="24a1d-123">Si vous n’utilisez pas les membres de données étendus, vous pouvez utiliser la structure des [**\_ \_ parms Open parms**](mci-open-parms.md) au lieu de l' **\_ \_ ouverture \_ des sons MCI** .</span><span class="sxs-lookup"><span data-stu-id="24a1d-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a1d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24a1d-124">Requirements</span></span>



| <span data-ttu-id="24a1d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24a1d-125">Requirement</span></span> | <span data-ttu-id="24a1d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="24a1d-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="24a1d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24a1d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24a1d-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24a1d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="24a1d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24a1d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24a1d-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24a1d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="24a1d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="24a1d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a1d-132"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a1d-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a1d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24a1d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a1d-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="24a1d-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="24a1d-135">**Structures MCI**</span><span class="sxs-lookup"><span data-stu-id="24a1d-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="24a1d-136">**MCI \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="24a1d-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="24a1d-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24a1d-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24a1d-138">**les \_ PARMS ouverts MCI \_**</span><span class="sxs-lookup"><span data-stu-id="24a1d-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 


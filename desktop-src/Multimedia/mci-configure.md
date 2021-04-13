---
title: Commande MCI_CONFIGURE (mmsystem. h)
description: La \_ commande MCI configurer affiche une boîte de dialogue permettant de définir les options de fonctionnement. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- Commande MCI_CONFIGURE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383983"
---
# <a name="mci_configure-command"></a><span data-ttu-id="40001-105">\_Commande MCI configurer</span><span class="sxs-lookup"><span data-stu-id="40001-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="40001-106">La \_ commande MCI configurer affiche une boîte de dialogue permettant de définir les options de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="40001-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="40001-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="40001-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="40001-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="40001-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="40001-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40001-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40001-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="40001-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="40001-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="40001-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="40001-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="40001-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="40001-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="40001-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="40001-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="40001-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="40001-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span><span class="sxs-lookup"><span data-stu-id="40001-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="40001-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="40001-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="40001-117">(Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="40001-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40001-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40001-118">Return Value</span></span>

<span data-ttu-id="40001-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="40001-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="40001-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40001-120">Requirements</span></span>



| <span data-ttu-id="40001-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40001-121">Requirement</span></span> | <span data-ttu-id="40001-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="40001-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40001-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40001-123">Minimum supported client</span></span><br/> | <span data-ttu-id="40001-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40001-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40001-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40001-125">Minimum supported server</span></span><br/> | <span data-ttu-id="40001-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40001-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="40001-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="40001-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="40001-128"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40001-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40001-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40001-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40001-130">MCI</span><span class="sxs-lookup"><span data-stu-id="40001-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="40001-131">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="40001-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


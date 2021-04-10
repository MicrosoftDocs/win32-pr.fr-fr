---
title: Commande MCI_MONITOR (mmsystem. h)
description: La \_ commande MCI Monitor spécifie la source de la présentation. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Commande MCI_MONITOR Windows multimédia
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942436"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="00ecd-105">\_Commande MCI Monitor</span><span class="sxs-lookup"><span data-stu-id="00ecd-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="00ecd-106">La \_ commande MCI Monitor spécifie la source de la présentation.</span><span class="sxs-lookup"><span data-stu-id="00ecd-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="00ecd-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="00ecd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="00ecd-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="00ecd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="00ecd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00ecd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ecd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="00ecd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="00ecd-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="00ecd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="00ecd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="00ecd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="00ecd-113">MCI \_ Notify, MCI \_ Wait ou MCI \_ test.</span><span class="sxs-lookup"><span data-stu-id="00ecd-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="00ecd-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="00ecd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="00ecd-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span><span class="sxs-lookup"><span data-stu-id="00ecd-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="00ecd-116">Pointeur vers une structure [**MCI \_ DGV \_ Monitor \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .</span><span class="sxs-lookup"><span data-stu-id="00ecd-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ecd-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00ecd-117">Return Value</span></span>

<span data-ttu-id="00ecd-118">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="00ecd-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ecd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="00ecd-119">Remarks</span></span>

<span data-ttu-id="00ecd-120">Les indicateurs supplémentaires suivants s’appliquent aux périphériques vidéo numériques :</span><span class="sxs-lookup"><span data-stu-id="00ecd-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="00ecd-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_méthode d' \_ analyse \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="00ecd-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="00ecd-122">Une constante indiquant que la méthode de surveillance est incluse dans le membre **dwMethod** de la structure identifiée par *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="00ecd-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="00ecd-123">Lorsque l' \_ \_ indicateur d’entrée du moniteur MCI DGV \_ est utilisé dans le membre **dwSource** , cela sélectionne la méthode de surveillance.</span><span class="sxs-lookup"><span data-stu-id="00ecd-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="00ecd-124">En règle générale, les différentes méthodes d’analyse ont des implications différentes sur la façon dont le matériel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="00ecd-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="00ecd-125">La méthode d’analyse par défaut est sélectionnée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00ecd-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="00ecd-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_source du \_ moniteur MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="00ecd-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="00ecd-127">Une constante indiquant que la source du moniteur est incluse dans le membre **dwSource** de la structure identifiée par *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="00ecd-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00ecd-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00ecd-128">Requirements</span></span>



| <span data-ttu-id="00ecd-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00ecd-129">Requirement</span></span> | <span data-ttu-id="00ecd-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="00ecd-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ecd-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00ecd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="00ecd-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00ecd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00ecd-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00ecd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="00ecd-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00ecd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00ecd-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="00ecd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ecd-136"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00ecd-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ecd-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ecd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ecd-138">MCI</span><span class="sxs-lookup"><span data-stu-id="00ecd-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="00ecd-139">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="00ecd-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


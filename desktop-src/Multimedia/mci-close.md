---
title: Commande MCI_CLOSE (mmsystem. h)
description: La \_ commande MCI Close libère l’accès à un appareil ou à un fichier. Tous les appareils reconnaissent cette commande.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- Commande MCI_CLOSE Windows multimédia
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103444"
---
# <a name="mci_close-command"></a><span data-ttu-id="8c6c5-105">\_Commande MCI Close</span><span class="sxs-lookup"><span data-stu-id="8c6c5-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="8c6c5-106">La \_ commande MCI Close libère l’accès à un appareil ou à un fichier.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="8c6c5-107">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-107">All devices recognize this command.</span></span>

<span data-ttu-id="8c6c5-108">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="8c6c5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c6c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6c5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8c6c5-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8c6c5-111">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8c6c5-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8c6c5-113">\_Attente MCI Notify ou MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8c6c5-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="8c6c5-114">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8c6c5-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c6c5-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span><span class="sxs-lookup"><span data-stu-id="8c6c5-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="8c6c5-116">Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8c6c5-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8c6c5-117">(Vous pouvez également utiliser une structure **MCI \_ Close \_ PARMS** .</span><span class="sxs-lookup"><span data-stu-id="8c6c5-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="8c6c5-118">Pour plus d’informations, consultez les commentaires pour les **\_ \_ PARMS génériques MCI**.)</span><span class="sxs-lookup"><span data-stu-id="8c6c5-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c6c5-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c6c5-119">Return Value</span></span>

<span data-ttu-id="8c6c5-120">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6c5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8c6c5-121">Remarks</span></span>

<span data-ttu-id="8c6c5-122">Le fait de quitter une application sans fermer les périphériques MCI ouverts peut rendre l’appareil inaccessible.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="8c6c5-123">Votre application doit fermer explicitement chaque appareil ou fichier une fois qu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="8c6c5-124">MCI décharge l’appareil lorsque toutes les instances de l’appareil ou tous les fichiers associés sont fermés.</span><span class="sxs-lookup"><span data-stu-id="8c6c5-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6c5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c6c5-125">Requirements</span></span>



| <span data-ttu-id="8c6c5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c6c5-126">Requirement</span></span> | <span data-ttu-id="8c6c5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c6c5-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6c5-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c6c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6c5-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c6c5-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8c6c5-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c6c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6c5-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c6c5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8c6c5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c6c5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6c5-133"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c6c5-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c6c5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c6c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6c5-135">MCI</span><span class="sxs-lookup"><span data-stu-id="8c6c5-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8c6c5-136">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="8c6c5-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


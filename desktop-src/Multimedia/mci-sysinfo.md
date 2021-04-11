---
title: Commande MCI_SYSINFO (mmsystem. h)
description: La \_ commande MCI sysinfo récupère des informations sur les périphériques MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Commande MCI_SYSINFO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942237"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="bee5d-104">\_Commande MCI sysinfo</span><span class="sxs-lookup"><span data-stu-id="bee5d-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="bee5d-105">La \_ commande MCI sysinfo récupère des informations sur les périphériques MCI.</span><span class="sxs-lookup"><span data-stu-id="bee5d-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="bee5d-106">MCI prend en charge cette commande directement au lieu de la transmettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bee5d-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="bee5d-107">Toute application MCI peut utiliser cette commande.</span><span class="sxs-lookup"><span data-stu-id="bee5d-107">Any MCI application can use this command.</span></span> <span data-ttu-id="bee5d-108">Les informations de chaîne sont retournées dans la mémoire tampon fournie par l’application vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="bee5d-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="bee5d-109">Les informations numériques sont retournées sous la forme d’une valeur **DWORD** placée dans la mémoire tampon fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="bee5d-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="bee5d-110">Le membre **dwRetSize** spécifie la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bee5d-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="bee5d-111">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="bee5d-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bee5d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bee5d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bee5d-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="bee5d-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-114">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="bee5d-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="bee5d-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-116">Un ou plusieurs des indicateurs standard et spécifiques à la commande suivants :</span><span class="sxs-lookup"><span data-stu-id="bee5d-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>\_INSTALLNAME MCI sysinfo \_</span><span class="sxs-lookup"><span data-stu-id="bee5d-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-118">Obtient le nom (indiqué dans le registre ou le fichier SYSTEM.INI) utilisé pour installer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bee5d-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nom MCI sysinfo \_</span><span class="sxs-lookup"><span data-stu-id="bee5d-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-120">Obtient un nom de périphérique correspondant au numéro d’appareil spécifié dans le membre **dwNumber** de la structure identifiée par **lpSysInfo**.</span><span class="sxs-lookup"><span data-stu-id="bee5d-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="bee5d-121">Si l' \_ \_ indicateur d’ouverture MCI sysinfo est défini, MCI retourne les noms des appareils ouverts.</span><span class="sxs-lookup"><span data-stu-id="bee5d-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ sysinfo \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="bee5d-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-123">Obtient la quantité ou le nom des appareils ouverts.</span><span class="sxs-lookup"><span data-stu-id="bee5d-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantité MCI sysinfo \_</span><span class="sxs-lookup"><span data-stu-id="bee5d-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-125">Obtient le nombre d’appareils du type spécifié qui sont répertoriés dans le registre ou la \[ section MCI \] du fichier SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="bee5d-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="bee5d-126">Si l' \_ \_ indicateur d’ouverture MCI sysinfo est défini, le nombre d’appareils ouverts est retourné.</span><span class="sxs-lookup"><span data-stu-id="bee5d-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="bee5d-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span><span class="sxs-lookup"><span data-stu-id="bee5d-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="bee5d-128">Pointeur vers une structure de valeur [**MCI \_ sysinfo \_**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="bee5d-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bee5d-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bee5d-129">Return Value</span></span>

<span data-ttu-id="bee5d-130">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="bee5d-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bee5d-131">Notes</span><span class="sxs-lookup"><span data-stu-id="bee5d-131">Remarks</span></span>

<span data-ttu-id="bee5d-132">Le membre **wDeviceType** de la structure identifiée par *lpSysInfo* est utilisé pour indiquer le type d’appareil de la requête.</span><span class="sxs-lookup"><span data-stu-id="bee5d-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="bee5d-133">Si le paramètre *wDeviceID* est défini sur MCI \_ All \_ Device \_ ID, il remplace la valeur de **wDeviceType**.</span><span class="sxs-lookup"><span data-stu-id="bee5d-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="bee5d-134">Pour obtenir la liste des types d’appareils, consultez [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="bee5d-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="bee5d-135">Les valeurs de retour de type entier sont des valeurs **DWORD** retournées dans la mémoire tampon vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="bee5d-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="bee5d-136">Les valeurs de retour de chaîne sont des chaînes terminées par le caractère null retournées dans la mémoire tampon vers laquelle pointe le membre **lpstrReturn** de la structure identifiée par *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="bee5d-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bee5d-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bee5d-137">Requirements</span></span>



| <span data-ttu-id="bee5d-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bee5d-138">Requirement</span></span> | <span data-ttu-id="bee5d-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee5d-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee5d-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bee5d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bee5d-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bee5d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bee5d-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bee5d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bee5d-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bee5d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bee5d-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="bee5d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="bee5d-145"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bee5d-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee5d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee5d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee5d-147">MCI</span><span class="sxs-lookup"><span data-stu-id="bee5d-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bee5d-148">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="bee5d-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


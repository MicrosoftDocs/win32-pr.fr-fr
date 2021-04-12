---
title: Commande MCI_GETDEVCAPS (mmsystem. h)
description: La \_ commande MCI GETDEVCAPS récupère des informations statiques sur un appareil.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Commande MCI_GETDEVCAPS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509418"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="1cffb-104">\_Commande MCI GETDEVCAPS</span><span class="sxs-lookup"><span data-stu-id="1cffb-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="1cffb-105">La \_ commande MCI GETDEVCAPS récupère des informations statiques sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="1cffb-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="1cffb-106">Tous les appareils reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="1cffb-106">All devices recognize this command.</span></span> <span data-ttu-id="1cffb-107">Les paramètres et indicateurs disponibles pour cette commande dépendent de l’appareil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1cffb-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="1cffb-108">Les informations sont retournées dans le membre **dwReturn** de la structure identifiée par *lpCapsParms*.</span><span class="sxs-lookup"><span data-stu-id="1cffb-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="1cffb-109">Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1cffb-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="1cffb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cffb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="1cffb-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-112">Identificateur de l’appareil MCI qui doit recevoir le message de commande.</span><span class="sxs-lookup"><span data-stu-id="1cffb-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="1cffb-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-114">MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1cffb-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="1cffb-115">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1cffb-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span><span class="sxs-lookup"><span data-stu-id="1cffb-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-117">Pointeur vers une structure [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="1cffb-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cffb-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1cffb-118">Return Value</span></span>

<span data-ttu-id="1cffb-119">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="1cffb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cffb-120">Notes</span><span class="sxs-lookup"><span data-stu-id="1cffb-120">Remarks</span></span>

<span data-ttu-id="1cffb-121">Les indicateurs standard et spécifiques à la commande suivants s’appliquent à tous les appareils prenant en charge MCI \_ GETDEVCAPS :</span><span class="sxs-lookup"><span data-stu-id="1cffb-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ périphérique composite MCI GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-123">Le membre **dwReturn** a la valeur **true** si l’appareil utilise le stockage de données qui doit être ouvert et fermé explicitement ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1cffb-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_type d' \_ appareil \_ GETDEVCAPS MCI</span><span class="sxs-lookup"><span data-stu-id="1cffb-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-125">Le membre **dwReturn** est défini sur l’une des valeurs indiquées dans [types d’appareils MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="1cffb-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ a un \_ son</span><span class="sxs-lookup"><span data-stu-id="1cffb-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-127">Le membre **dwReturn** a la valeur **true** si l’appareil a une sortie audio ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1cffb-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ a une \_ vidéo</span><span class="sxs-lookup"><span data-stu-id="1cffb-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-129">Le membre **dwReturn** a la valeur **true** si l’appareil a une sortie vidéo ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1cffb-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="1cffb-130">Par exemple, le membre a la valeur **true** pour les appareils qui prennent en charge le jeu de commandes videodisc.</span><span class="sxs-lookup"><span data-stu-id="1cffb-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_élément GETDEVCAPS \_ MCI</span><span class="sxs-lookup"><span data-stu-id="1cffb-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-132">Spécifie que le membre **dwItem** de la structure [**\_ \_ GETDEVCAPSs MCI**](mci-getdevcaps-parms.md) contient l’une des constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cffb-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ peut \_ éjecter</span><span class="sxs-lookup"><span data-stu-id="1cffb-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-134">Le membre **dwReturn** a la valeur **true** si l’appareil peut éjecter le média ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ peut \_ jouer</span><span class="sxs-lookup"><span data-stu-id="1cffb-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-136">Le membre **dwReturn** a la valeur **true** si l’appareil peut lire le média. dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="1cffb-137">Si un appareil spécifie la **valeur true**, cela signifie que l’appareil prend en charge les commandes [MCI \_ Pause](mci-pause.md) et [ \_ Stop MCI](mci-stop.md) , ainsi que la commande de [ \_ lecture MCI](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="1cffb-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ peut \_ Enregistrer</span><span class="sxs-lookup"><span data-stu-id="1cffb-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-139">Le membre **dwReturn** a la valeur **true** si l’appareil prend en charge l’enregistrement ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="1cffb-140">Si un appareil spécifie la **valeur true**, cela signifie que l’appareil prend en charge les \_ commandes de pause MCI et d’arrêt MCI, ainsi \_ que la commande d' [ \_ enregistrement MCI](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="1cffb-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ peut \_ Enregistrer</span><span class="sxs-lookup"><span data-stu-id="1cffb-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-142">Le membre **dwReturn** a la valeur **true** si l’appareil peut enregistrer un fichier ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ utilise des \_ fichiers</span><span class="sxs-lookup"><span data-stu-id="1cffb-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-144">Le membre **dwReturn** a la valeur **true** si l’appareil requiert un nom de fichier ; elle a la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1cffb-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="1cffb-145">Seuls les appareils composés utilisent des fichiers.</span><span class="sxs-lookup"><span data-stu-id="1cffb-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="1cffb-146">Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **Digitalvideo** :</span><span class="sxs-lookup"><span data-stu-id="1cffb-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut se \_ figer</span><span class="sxs-lookup"><span data-stu-id="1cffb-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-148">Le membre **dwReturn** a la valeur **true** si l’appareil peut geler des frames ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut être \_ verrouillé</span><span class="sxs-lookup"><span data-stu-id="1cffb-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-150">Le membre **dwReturn** a la valeur **true** si l’appareil peut se verrouiller ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>la \_ GETDEVCAPS DGV MCI \_ \_ peut être \_ inversée</span><span class="sxs-lookup"><span data-stu-id="1cffb-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-152">Le membre **dwReturn** a la valeur **true** si l’appareil peut jouer en sens inverse ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ peut être \_ Str \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-154">Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer l’entrée ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_DGV \_ GETDEVCAPS MCI \_ peut être \_ étiré</span><span class="sxs-lookup"><span data-stu-id="1cffb-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-156">Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer une image ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_test de \_ GETDEVCAPS \_ DGV \_ MCI</span><span class="sxs-lookup"><span data-stu-id="1cffb-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-158">Le membre **dwReturn** a la valeur **true** si l’appareil peut effectuer des tests ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ a \_ toujours</span><span class="sxs-lookup"><span data-stu-id="1cffb-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-160">Le membre **dwReturn** a la valeur **true** si l’appareil peut afficher des images fixes ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="1cffb-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-162">Le membre **dwReturn** est défini sur le nombre maximal de fenêtres que l’appareil peut gérer simultanément.</span><span class="sxs-lookup"><span data-stu-id="1cffb-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>débit maximal de MCI \_ DGV \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-164">Le membre **dwReturn** est défini sur la vitesse de lecture maximale pour l’appareil, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>taux minimal de MCI \_ DGV \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-166">Le membre **dwReturn** est défini sur la vitesse de lecture minimale de l’appareil, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ palettes MCI DGV GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-168">Le membre **dwReturn** a la valeur **true** si l’appareil peut retourner un handle de palette ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="1cffb-169">Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type de périphérique **VCR** :</span><span class="sxs-lookup"><span data-stu-id="1cffb-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>taux d’incrément de l' \_ horloge MCI GETDEVCAPS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-171">Le membre **dwReturn** est défini sur le nombre d’incréments par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ détecter une \_ longueur</span><span class="sxs-lookup"><span data-stu-id="1cffb-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-173">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de détecter la longueur du média. dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut se \_ figer</span><span class="sxs-lookup"><span data-stu-id="1cffb-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-175">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de figer l’image de sortie ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ surveiller les \_ sources</span><span class="sxs-lookup"><span data-stu-id="1cffb-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-177">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de surveiller les sources ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ préroll</span><span class="sxs-lookup"><span data-stu-id="1cffb-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-179">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité d’effectuer un préroll ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI \_ VCR \_ GETDEVCAPS \_ peut \_ prévisualiser</span><span class="sxs-lookup"><span data-stu-id="1cffb-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-181">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité d’afficher des préversions ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ inversé</span><span class="sxs-lookup"><span data-stu-id="1cffb-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-183">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de fonctionner en sens inverse. dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ peut être \_ testé</span><span class="sxs-lookup"><span data-stu-id="1cffb-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-185">Le membre **dwReturn** a la valeur **true** si l’appareil est en capacité de tester ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ magnétoscope \_ GETDEVCAPS \_ avec \_ horloge</span><span class="sxs-lookup"><span data-stu-id="1cffb-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-187">Le membre **dwReturn** a la valeur **true** si l’appareil prend en charge une horloge externe. dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>le \_ magnétoscope MCI \_ GETDEVCAPS \_ a un \_ code temporel</span><span class="sxs-lookup"><span data-stu-id="1cffb-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-189">Le membre **dwReturn** a la valeur **true** si l’appareil dispose d’une fonctionnalité de code temporel ou si cette fonctionnalité est inconnue. dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_magnétoscope MCI \_ GETDEVCAPS \_ nombre \_ de \_ marques</span><span class="sxs-lookup"><span data-stu-id="1cffb-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-191">Le membre **dwReturn** est défini sur le nombre de marques (99).</span><span class="sxs-lookup"><span data-stu-id="1cffb-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>précision de la \_ recherche MCI VCR \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-193">Le membre **dwReturn** est défini sur la précision de la recherche de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1cffb-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="1cffb-194">Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil de **superposition** :</span><span class="sxs-lookup"><span data-stu-id="1cffb-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ OVLY \_ GETDEVCAPS \_ peut se \_ figer</span><span class="sxs-lookup"><span data-stu-id="1cffb-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-196">Le membre **dwReturn** a la valeur **true** si l’appareil peut geler l’image ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_OVLY \_ GETDEVCAPS MCI \_ peut être \_ étiré</span><span class="sxs-lookup"><span data-stu-id="1cffb-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-198">Le membre **dwReturn** a la valeur **true** si l’appareil peut étirer l’image pour remplir le frame ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows</span><span class="sxs-lookup"><span data-stu-id="1cffb-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-200">Le membre **dwReturn** est défini sur le nombre maximal de fenêtres que l’appareil peut gérer simultanément.</span><span class="sxs-lookup"><span data-stu-id="1cffb-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="1cffb-201">Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **videodisc** :</span><span class="sxs-lookup"><span data-stu-id="1cffb-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ peut \_ inverser</span><span class="sxs-lookup"><span data-stu-id="1cffb-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-203">Le membre **dwReturn** a la valeur **true** si le lecteur videodisc peut jouer en sens inverse ; dans le cas contraire, il est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1cffb-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="1cffb-204">Certains lecteurs peuvent lire des disques CLV à l’inverse, ainsi que des disques CAV.</span><span class="sxs-lookup"><span data-stu-id="1cffb-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ \_ GETDEVCAPS \_ CAV</span><span class="sxs-lookup"><span data-stu-id="1cffb-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-206">En cas de combinaison avec d’autres éléments, spécifie que les informations de retour s’appliquent au format CAV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="1cffb-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="1cffb-207">Il s’agit de la valeur par défaut si aucun videodisc n’est inséré.</span><span class="sxs-lookup"><span data-stu-id="1cffb-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ \_ GETDEVCAPS \_ CLV</span><span class="sxs-lookup"><span data-stu-id="1cffb-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-209">En cas de combinaison avec d’autres éléments, spécifie que les informations de retour s’appliquent au format CLV videodiscs.</span><span class="sxs-lookup"><span data-stu-id="1cffb-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ taux rapide de GETDEVCAPS MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-211">Le membre **dwReturn** est défini sur le taux de lecture rapide standard en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>taux normal de MCI \_ VD \_ GETDEVCAPS \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-213">Le membre **dwReturn** est défini sur la vitesse de lecture normale en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ taux lent de GETDEVCAPS MCI VD \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-215">Le membre **dwReturn** est défini sur le taux de lecture lent standard en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="1cffb-216">Les indicateurs suivants peuvent être spécifiés dans le membre **dwItem** de [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) pour le type d’appareil **WaveAudio** :</span><span class="sxs-lookup"><span data-stu-id="1cffb-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="1cffb-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_entrée MCI Wave \_ GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-218">Le membre **dwReturn** est défini sur le nombre total d’appareils d’entrée (enregistrement) de la forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="1cffb-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="1cffb-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_sortie MCI Wave \_ GETDEVCAPS \_</span><span class="sxs-lookup"><span data-stu-id="1cffb-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="1cffb-220">Le membre **dwReturn** est défini sur le nombre total d’appareils de sortie de forme d’onde (lecture).</span><span class="sxs-lookup"><span data-stu-id="1cffb-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1cffb-221">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cffb-221">Requirements</span></span>



| <span data-ttu-id="1cffb-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cffb-222">Requirement</span></span> | <span data-ttu-id="1cffb-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cffb-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cffb-224">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cffb-224">Minimum supported client</span></span><br/> | <span data-ttu-id="1cffb-225">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cffb-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1cffb-226">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cffb-226">Minimum supported server</span></span><br/> | <span data-ttu-id="1cffb-227">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cffb-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1cffb-228">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cffb-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cffb-229"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cffb-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cffb-230">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cffb-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cffb-231">MCI</span><span class="sxs-lookup"><span data-stu-id="1cffb-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1cffb-232">Commandes MCI</span><span class="sxs-lookup"><span data-stu-id="1cffb-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


---
title: Messages Bluetooth et WM_DEVICECHANGE
description: Bluetooth comprend des \_ messages DEVICECHANGE WM spécifiques qui permettent aux développeurs d’obtenir des messages lorsque des appareils Bluetooth subissent des modifications d’État.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941078"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="f3ca3-103">Messages Bluetooth et WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="f3ca3-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="f3ca3-104">Bluetooth comprend des [**messages \_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) spécifiques qui permettent aux développeurs d’obtenir des messages lorsque des appareils Bluetooth subissent des modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="f3ca3-105">Cette rubrique explique comment recevoir des messages **WM \_ DEVICECHANGE** spécifiques à Bluetooth et répertorie les messages spécifiques à Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="f3ca3-106">Réception de messages WM DEVICECHANGE spécifiques à Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="f3ca3-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="f3ca3-107">Pour recevoir les messages [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , vous devez d’abord ouvrir un descripteur de la radio locale.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="f3ca3-108">Pour ce faire, utilisez l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f3ca3-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="f3ca3-109">Utilisez la [fonction SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) avec les paramètres suivants : (GUID \_ BTHPORT \_ Device \_ interface,..., DIGCF \_ present \| DIGCF \_ DEVICEINTERFACE), puis utilisez les fonctions [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)et [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .</span><span class="sxs-lookup"><span data-stu-id="f3ca3-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="f3ca3-110">Utilisez les fonctions [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)et [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .</span><span class="sxs-lookup"><span data-stu-id="f3ca3-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="f3ca3-111">Lorsque le handle radio Bluetooth est ouvert, appelez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) et inscrivez-vous aux notifications sur le handle à l’aide du **\_ \_ handle DBT DEVTYP** en tant que DeviceType.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="f3ca3-112">Lorsqu’ils sont inscrits, les GUID suivants sont envoyés et le membre de **\_ données** [**\_ \_ handle Broadcast handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: dbch est la mémoire tampon associée.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="f3ca3-113">Messages spécifiques à Bluetooth</span><span class="sxs-lookup"><span data-stu-id="f3ca3-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="f3ca3-114">Le tableau suivant répertorie les messages [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) spécifiques à Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="f3ca3-115">GUID</span><span class="sxs-lookup"><span data-stu-id="f3ca3-115">GUID</span></span>                                   | <span data-ttu-id="f3ca3-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="f3ca3-116">BUFFER</span></span>                                                  | <span data-ttu-id="f3ca3-117">Description</span><span class="sxs-lookup"><span data-stu-id="f3ca3-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3ca3-118">événement de GUID \_ Bluetooth \_ HCI \_</span><span class="sxs-lookup"><span data-stu-id="f3ca3-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="f3ca3-119">**\_ \_ informations sur l’événement HCI BTH \_**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="f3ca3-120">Ce message est envoyé lorsqu’un appareil Bluetooth distant se connecte ou se déconnecte au niveau de la liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f3ca3-121">\_ \_ Événement L2CAP de GUID Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="f3ca3-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="f3ca3-122">**\_ \_ Informations sur l’événement BTH L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="f3ca3-123">Ce message est envoyé lorsqu’un canal L2CAP entre la radio locale et un périphérique Bluetooth distant a été établi ou arrêté.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="f3ca3-124">Pour les canaux L2CAP qui sont des multiplexeurs, tels que RFCOMM, ce message est envoyé uniquement lorsque le canal sous-jacent est établi, et non lorsque chaque canal multiplexé, tel qu’un canal RFCOMM, est établi ou arrêté.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="f3ca3-125">\_demande de \_ code confidentiel Bluetooth GUID \_</span><span class="sxs-lookup"><span data-stu-id="f3ca3-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="f3ca3-126">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-126">Not applicable.</span></span>                                         | <span data-ttu-id="f3ca3-127">Ce message doit être ignoré par l’application.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-127">This message should be ignored by the application.</span></span> <span data-ttu-id="f3ca3-128">Si l’application doit recevoir des demandes de code confidentiel, la fonction [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="f3ca3-129">\_radio Bluetooth \_ GUID \_ dans la \_ plage</span><span class="sxs-lookup"><span data-stu-id="f3ca3-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="f3ca3-130">**\_ \_ zone de radio BTH dans la \_ plage**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="f3ca3-131">Ce message est envoyé lorsque l’un des attributs suivants d’un appareil Bluetooth distant a changé : l’appareil a été découvert, la classe de l’appareil, le nom, l’état connecté ou l’état de mémorisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="f3ca3-132">Ce message est également envoyé lorsque ces attributs sont définis ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="f3ca3-133">la \_ radio Bluetooth GUID est \_ \_ hors \_ \_ limites</span><span class="sxs-lookup"><span data-stu-id="f3ca3-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="f3ca3-134">**\_adresse Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="f3ca3-135">Ce message est envoyé lorsqu’un appareil précédemment détecté n’a pas été trouvé après la dernière recherche.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="f3ca3-136">Ce message ne sera pas envoyé pour les appareils mémorisés.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="f3ca3-137">La structure d' **\_ adresse BTH** est l’adresse de l’appareil qui n’a pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="f3ca3-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="f3ca3-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3ca3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3ca3-139">**BluetoothFindFirstRadio**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="f3ca3-140">**BluetoothFindNextRadio**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="f3ca3-141">**BluetoothFindRadioClose**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="f3ca3-142">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="f3ca3-143">SetupDiDestroyDeviceInfoList</span><span class="sxs-lookup"><span data-stu-id="f3ca3-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="f3ca3-144">SetupDiEnumDeviceInterfaces</span><span class="sxs-lookup"><span data-stu-id="f3ca3-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="f3ca3-145">SetupDiGetClassDevs</span><span class="sxs-lookup"><span data-stu-id="f3ca3-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="f3ca3-146">**\_adresse Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="f3ca3-147">**\_ \_ informations sur l’événement HCI BTH \_**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="f3ca3-148">**\_ \_ Informations sur l’événement BTH L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="f3ca3-149">**\_ \_ zone de radio BTH dans la \_ plage**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="f3ca3-150">**\_handle de diffusion dev \_**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="f3ca3-151">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="f3ca3-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 
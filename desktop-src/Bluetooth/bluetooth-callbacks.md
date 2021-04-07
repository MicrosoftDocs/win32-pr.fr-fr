---
title: Rappels Bluetooth
description: Les fonctions de rappel Bluetooth de cette section sont utilisées en association avec les fonctions qui permettent de gérer les appareils et les services Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671609"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="b9c09-103">Rappels Bluetooth</span><span class="sxs-lookup"><span data-stu-id="b9c09-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="b9c09-104">Les fonctions de rappel Bluetooth de cette section sont utilisées en association avec les fonctions qui permettent de gérer les appareils et les services Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b9c09-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="b9c09-105">Bluetooth est également pris en charge à l’aide de l’interface de programmation Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="b9c09-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="b9c09-106">Pour plus d’informations sur la programmation de Bluetooth à l’aide de l’interface Windows Sockets, consultez [prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="b9c09-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="b9c09-107">Section</span><span class="sxs-lookup"><span data-stu-id="b9c09-107">Section</span></span>                                                                                      | <span data-ttu-id="b9c09-108">Content</span><span class="sxs-lookup"><span data-stu-id="b9c09-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9c09-109">**\_rappel d’authentification PFN \_**</span><span class="sxs-lookup"><span data-stu-id="b9c09-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="b9c09-110">Utilisé conjointement avec la fonction [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="b9c09-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="b9c09-111">**\_rappel d’authentification PFN \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="b9c09-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="b9c09-112">Utilisé conjointement avec la fonction [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .</span><span class="sxs-lookup"><span data-stu-id="b9c09-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="b9c09-113">**\_rappel des \_ attributs d’énumération Bluetooth PFN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9c09-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="b9c09-114">Appelée une fois pour chaque attribut trouvé dans le paramètre *pSDPStream* qui est passé à l’appel de fonction [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) .</span><span class="sxs-lookup"><span data-stu-id="b9c09-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="b9c09-115">**rappel de l' \_ appareil PFN \_**</span><span class="sxs-lookup"><span data-stu-id="b9c09-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="b9c09-116">Utilisé en association avec la sélection des appareils Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b9c09-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 





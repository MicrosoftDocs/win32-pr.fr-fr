---
title: Interfaces COM-accès de l’appareil
description: Interfaces COM (Component Object Model) dans l’API d’accès à l’appareil.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032053"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="70b59-103">Interfaces COM-accès de l’appareil</span><span class="sxs-lookup"><span data-stu-id="70b59-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="70b59-104">Interfaces COM (Component Object Model) dans l’API d’accès à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70b59-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70b59-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="70b59-105">In this section</span></span>

| <span data-ttu-id="70b59-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="70b59-106">Topic</span></span> | <span data-ttu-id="70b59-107">Description</span><span class="sxs-lookup"><span data-stu-id="70b59-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="70b59-108">**ICreateDeviceAccessAsync**</span><span class="sxs-lookup"><span data-stu-id="70b59-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="70b59-109">L’interface [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) est retournée à partir d’un appel à CreateDeviceAccessInstance.</span><span class="sxs-lookup"><span data-stu-id="70b59-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="70b59-110">Elle permet à l’appelant de contrôler le fonctionnement de la liaison à une instance d’un appareil afin de récupérer une autre interface qui peut être utilisée pour interagir avec cet appareil.</span><span class="sxs-lookup"><span data-stu-id="70b59-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="70b59-111">**IDeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="70b59-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="70b59-112">Envoie un code de contrôle à un pilote de périphérique. Cette action amène l’appareil à effectuer l’opération correspondante.</span><span class="sxs-lookup"><span data-stu-id="70b59-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="70b59-113">**IDeviceRequestCompletionCallback**</span><span class="sxs-lookup"><span data-stu-id="70b59-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="70b59-114">Fournit une méthode pour gérer l’achèvement des appels à la méthode [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).</span><span class="sxs-lookup"><span data-stu-id="70b59-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="70b59-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70b59-115">Related topics</span></span>

<span data-ttu-id="70b59-116">[Exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications pour appareils UWP pour appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="70b59-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>

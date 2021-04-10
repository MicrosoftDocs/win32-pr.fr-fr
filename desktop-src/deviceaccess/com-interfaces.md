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
# <a name="com-interfaces---device-access"></a>Interfaces COM-accès de l’appareil

Interfaces COM (Component Object Model) dans l’API d’accès à l’appareil.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | L’interface [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) est retournée à partir d’un appel à CreateDeviceAccessInstance. Elle permet à l’appelant de contrôler le fonctionnement de la liaison à une instance d’un appareil afin de récupérer une autre interface qui peut être utilisée pour interagir avec cet appareil.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Envoie un code de contrôle à un pilote de périphérique. Cette action amène l’appareil à effectuer l’opération correspondante. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Fournit une méthode pour gérer l’achèvement des appels à la méthode [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications pour appareils UWP pour appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)

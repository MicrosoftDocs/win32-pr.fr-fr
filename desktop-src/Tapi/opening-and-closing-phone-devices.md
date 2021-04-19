---
description: Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Ouverture et fermeture des appareils téléphoniques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544707"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="59d6a-103">Ouverture et fermeture des appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="59d6a-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="59d6a-104">Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone.</span><span class="sxs-lookup"><span data-stu-id="59d6a-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="59d6a-105">Une fois qu’un appareil téléphonique a été ouvert avec succès, l’application est retournée en tant que handle représentant le téléphone ouvert.</span><span class="sxs-lookup"><span data-stu-id="59d6a-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="59d6a-106">Un appareil téléphonique peut être ouvert dans différents modes, fournissant ainsi un moyen structuré de partager un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="59d6a-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="59d6a-107">La fonction [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) ouvre l’appareil téléphonique spécifié pour permettre à l’application d’accéder aux fonctions sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="59d6a-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="59d6a-108">Un appareil téléphonique est identifié comme **phoneOpen** à l’aide de son identificateur d’appareil, qui est passé comme paramètre *dwDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="59d6a-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 




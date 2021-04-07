---
title: API du périphérique logiciel
description: Vous pouvez utiliser l’API de périphérique logiciel pour créer un appareil PnP à partir d’une application.
ms.assetid: 203abb2c-526f-4995-95de-4eb0ecee63d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e011d806ea21310fccc6ca96517a5465cb41add1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729708"
---
# <a name="software-device-api"></a><span data-ttu-id="99086-103">API du périphérique logiciel</span><span class="sxs-lookup"><span data-stu-id="99086-103">Software Device API</span></span>

## <a name="purpose"></a><span data-ttu-id="99086-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="99086-104">Purpose</span></span>

<span data-ttu-id="99086-105">Vous pouvez utiliser l’API de périphérique logiciel pour créer un appareil PnP à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="99086-105">You can use the Software Device API to create a PnP device from an app.</span></span> <span data-ttu-id="99086-106">L’API vous permet d’énumérer l’appareil en tant qu’enfant d’un appareil parent existant.</span><span class="sxs-lookup"><span data-stu-id="99086-106">The API lets you enumerate the device as a child of any existing parent device.</span></span> <span data-ttu-id="99086-107">L’API vous permet également d’inscrire des interfaces de périphérique sur les appareils énumérés et de définir les propriétés des appareils et des interfaces.</span><span class="sxs-lookup"><span data-stu-id="99086-107">The API also lets you register device interfaces against the enumerated devices and set properties for the devices and interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99086-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="99086-108">In this section</span></span>



| <span data-ttu-id="99086-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="99086-109">Topic</span></span>                                                                                         | <span data-ttu-id="99086-110">Description</span><span class="sxs-lookup"><span data-stu-id="99086-110">Description</span></span>                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99086-111">[Guide de programmation de l’API de périphérique logiciel](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99086-111">[Software Device API Programming Guide](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span></span><br/> | <span data-ttu-id="99086-112">Ce guide contient des informations sur l’utilisation de l’API de périphérique logiciel pour énumérer les périphériques PnP.</span><span class="sxs-lookup"><span data-stu-id="99086-112">This guide contains info on how to use the Software Device API to enumerate PnP devices.</span></span> <br/>                                                                               |
| [<span data-ttu-id="99086-113">Informations de référence sur l’API de périphérique logiciel</span><span class="sxs-lookup"><span data-stu-id="99086-113">Software Device API Reference</span></span>](software-device-api-reference.md)<br/>                 | <span data-ttu-id="99086-114">Cette référence décrit les fonctions de l’API du périphérique logiciel qu’une application cliente appelle et une fonction de rappel qu’une application cliente implémente et les structures de l’API du périphérique logiciel.</span><span class="sxs-lookup"><span data-stu-id="99086-114">This reference describes Software Device API functions that a client app calls and a callback function that a client app implements and Software Device API structures.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="99086-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="99086-115">Developer audience</span></span>

<span data-ttu-id="99086-116">L’API du périphérique logiciel est conçue pour être utilisée par les développeurs qui souhaitent publier des fonctionnalités d’appareil dans le « répertoire » PnP ou pour charger un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="99086-116">The Software Device API is designed for use by developers who want to publish device functionality in the PnP "directory" or to load a device driver.</span></span>

 

 

[<span data-ttu-id="99086-117">Envoyer des commentaires sur cette rubrique à Microsoft</span><span class="sxs-lookup"><span data-stu-id="99086-117">Send comments about this topic to Microsoft</span></span>](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Envoyer des commentaires sur cette rubrique à Microsoft")
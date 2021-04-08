---
description: Les fournisseurs de paquets réseau (NPPs) exposent les interfaces IDelaydC, IESP, IRTC et IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Sélection d’une interface NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864058"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="03060-103">Sélection d’une interface NPP</span><span class="sxs-lookup"><span data-stu-id="03060-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="03060-104">Les fournisseurs de paquets réseau (NPPs) exposent les interfaces [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md)et [**IStats**](istats.md) .</span><span class="sxs-lookup"><span data-stu-id="03060-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="03060-105">Chacune de ces interfaces fournit des méthodes similaires pour connecter le NPP au réseau, capturer le trafic réseau et collecter des informations statistiques sur les données capturées.</span><span class="sxs-lookup"><span data-stu-id="03060-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="03060-106">Pour choisir l’interface à utiliser, reportez-vous au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03060-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="03060-107">Lorsque vous connectez un NPP au réseau avec l’une de ces interfaces, vous pouvez utiliser uniquement les méthodes fournies par cette interface.</span><span class="sxs-lookup"><span data-stu-id="03060-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="03060-108">Par exemple, si vous vous connectez au réseau à l’aide de l’interface [**IRTC**](irtc.md) , puis que vous essayez de démarrer une capture avec [**IDelaydC**](idelaydc.md), votre appel pour démarrer la capture échoue et un code d’erreur est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="03060-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="03060-109">Interface</span><span class="sxs-lookup"><span data-stu-id="03060-109">Interface</span></span>                    | <span data-ttu-id="03060-110">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="03060-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03060-111">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="03060-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="03060-112">Utilisez pour capturer le trafic réseau et le stocker dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="03060-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="03060-113">Cette interface est utilisée par l’interface utilisateur Moniteur réseau et d’autres applications NPP, qui requièrent le stockage des informations réseau capturées.</span><span class="sxs-lookup"><span data-stu-id="03060-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="03060-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="03060-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="03060-115">Utilisé pour fournir des statistiques améliorées dans un format de fichier ESP spécial.</span><span class="sxs-lookup"><span data-stu-id="03060-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="03060-116">Cette interface est utilisée par les applications NPP qui nécessitent les statistiques améliorées fournies par le format ESP.</span><span class="sxs-lookup"><span data-stu-id="03060-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="03060-117">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="03060-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="03060-118">Utilisez pour capturer le trafic réseau en temps réel et déclencher des événements lorsqu’ils se produisent.</span><span class="sxs-lookup"><span data-stu-id="03060-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="03060-119">Cette interface est utilisée par les applications NPP qui requièrent des captures au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="03060-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="03060-120">Notez que cette interface ne fournit pas les statistiques fournies par les autres interfaces NPP, pas plus qu’elle ne vous permet d’insérer des frames dans le trafic réseau capturé.</span><span class="sxs-lookup"><span data-stu-id="03060-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="03060-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="03060-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="03060-122">Utilisez pour récupérer des statistiques de capture, mais pas les frames capturés.</span><span class="sxs-lookup"><span data-stu-id="03060-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 





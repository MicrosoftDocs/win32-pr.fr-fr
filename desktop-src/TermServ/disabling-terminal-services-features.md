---
title: Désactivation des fonctionnalités de Services Bureau à distance
description: Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/01/2020
ms.locfileid: "103941547"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="71dc4-103">Désactivation des fonctionnalités de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="71dc4-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="71dc4-104">Pour renforcer la sécurité, vous pouvez choisir de désactiver les fonctionnalités de Services Bureau à distance telles que la redirection du presse-papiers et la redirection de l’imprimante pour les clients qui se connectent aux serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) à l’aide du contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="71dc4-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="71dc4-105">**Pour désactiver les fonctionnalités de Services Bureau à distance**</span><span class="sxs-lookup"><span data-stu-id="71dc4-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="71dc4-106">Modifiez le registre de l’ordinateur client et ajoutez les clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="71dc4-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="71dc4-107">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**</span><span class="sxs-lookup"><span data-stu-id="71dc4-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="71dc4-108">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**</span><span class="sxs-lookup"><span data-stu-id="71dc4-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="71dc4-109">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**</span><span class="sxs-lookup"><span data-stu-id="71dc4-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="71dc4-110">Affectez la valeur **reg \_ DWORD** 1 à la valeur des deux clés.</span><span class="sxs-lookup"><span data-stu-id="71dc4-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 





---
description: Si cette stratégie système par ordinateur est définie sur 1, la possibilité d’utiliser l’interface utilisateur intégrée est désactivée sur l’ordinateur. La valeur par défaut est 0, ce qui active la fonctionnalité de gestionnaires d’interface utilisateur incorporés.
ms.assetid: f69d69a3-3c28-4841-a334-3acb61a06bc2
title: MsiDisableEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f5bfe6abfbb386253631c2858dab6ef36bcf39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953081"
---
# <a name="msidisableembeddedui"></a><span data-ttu-id="65b2f-104">MsiDisableEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="65b2f-104">MsiDisableEmbeddedUI</span></span>

<span data-ttu-id="65b2f-105">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur 1, la possibilité d’utiliser l’interface utilisateur intégrée est désactivée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="65b2f-105">If this per-machine [system policy](system-policy.md) is set to 1, the capability to use embedded UI is disabled on the computer.</span></span> <span data-ttu-id="65b2f-106">La valeur par défaut est 0, ce qui active la fonctionnalité de gestionnaires d’interface utilisateur incorporés.</span><span class="sxs-lookup"><span data-stu-id="65b2f-106">The default value is 0, which enables the embedded UI handlers capability.</span></span>

<span data-ttu-id="65b2f-107">Pour désactiver l’interface utilisateur incorporée pour un package unique, vous pouvez utiliser la propriété [**MSIDISABLEEEUI**](msidisableeeui.md) .</span><span class="sxs-lookup"><span data-stu-id="65b2f-107">To disable the embedded UI for a single package, you can use the [**MSIDISABLEEEUI**](msidisableeeui.md) property.</span></span>

<span data-ttu-id="65b2f-108">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="65b2f-108">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="65b2f-109">Cette fonction est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="65b2f-109">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="65b2f-110">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="65b2f-110">Registry Key</span></span>

<span data-ttu-id="65b2f-111">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="65b2f-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="65b2f-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="65b2f-112">Data Type</span></span>

<span data-ttu-id="65b2f-113">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="65b2f-113">**REG\_DWORD**</span></span>

 

 




---
description: Si cette stratégie système par ordinateur est définie sur 1, aucun package sur le système n’obtient la fonctionnalité de composant partagé activée par l’attribut msidbComponentAttributesShared dans la table des composants.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527039"
---
# <a name="disablesharedcomponent"></a><span data-ttu-id="fe73c-103">DisableSharedComponent</span><span class="sxs-lookup"><span data-stu-id="fe73c-103">DisableSharedComponent</span></span>

<span data-ttu-id="fe73c-104">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur 1, aucun package sur le système n’obtient la fonctionnalité de composant partagé activée par l’attribut **msidbComponentAttributesShared** dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe73c-104">If this per-machine [system policy](system-policy.md) is set to 1, no package on the system gets the shared component functionality enabled by the **msidbComponentAttributesShared** attribute in the [Component table](component-table.md).</span></span> <span data-ttu-id="fe73c-105">La valeur par défaut est 0, ce qui active la fonctionnalité de composant partagé pour les composants marqués avec **msidbComponentAttributesShared** dans tous les packages.</span><span class="sxs-lookup"><span data-stu-id="fe73c-105">The default value is 0, which enables the shared component functionality for components marked with **msidbComponentAttributesShared** in all packages.</span></span>

<span data-ttu-id="fe73c-106">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fe73c-106">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="fe73c-107">Cette fonction est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="fe73c-107">This function is available beginning with Windows Installer 4.5.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fe73c-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="fe73c-108">Registry Key</span></span>

<span data-ttu-id="fe73c-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="fe73c-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fe73c-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="fe73c-110">Data Type</span></span>

<span data-ttu-id="fe73c-111">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="fe73c-111">**REG\_DWORD**</span></span>

 

 




---
description: Si cette stratégie système est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951329"
---
# <a name="disablerollback"></a><span data-ttu-id="7593e-103">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="7593e-103">DisableRollback</span></span>

<span data-ttu-id="7593e-104">Si cette [stratégie système](system-policy.md) est définie sur 1, le programme d’installation ne stocke pas les fichiers de restauration lors de l’installation et désactive la restauration de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7593e-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="7593e-105">Par défaut, la restauration est activée.</span><span class="sxs-lookup"><span data-stu-id="7593e-105">By default, rollback is enabled.</span></span> <span data-ttu-id="7593e-106">Les administrateurs sont invités à ne pas utiliser cette stratégie, sauf si elle est absolument essentielle.</span><span class="sxs-lookup"><span data-stu-id="7593e-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="7593e-107">Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="7593e-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="7593e-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="7593e-108">Registry Key</span></span>

<span data-ttu-id="7593e-109">Pour désactiver la restauration des installations par utilisateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="7593e-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="7593e-110">**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="7593e-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="7593e-111">Pour désactiver la restauration des installations par ordinateur, affectez la valeur 1 à **DisableRollback** sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="7593e-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="7593e-112">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="7593e-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7593e-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="7593e-113">Data Type</span></span>

<span data-ttu-id="7593e-114">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="7593e-114">**REG\_DWORD**</span></span>

 

 




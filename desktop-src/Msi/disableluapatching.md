---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation empêche les non-administrateurs d’utiliser la mise à jour corrective du contrôle de compte d’utilisateur (UAC) pour n’importe quelle application installée sur l’ordinateur.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535080"
---
# <a name="disableluapatching"></a><span data-ttu-id="2759b-103">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="2759b-103">DisableLUAPatching</span></span>

<span data-ttu-id="2759b-104">Si cette stratégie système par ordinateur est définie sur « 1 », le programme d’installation empêche les non-administrateurs d’utiliser la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour les applications installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2759b-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="2759b-105">Lorsque la stratégie système par ordinateur n’est pas définie ou définie sur 0, les non-administrateurs peuvent appliquer des correctifs utilisateur de moindre privilège aux applications qui sont activées pour la mise à jour corrective des comptes d’utilisateur de moindre privilège.</span><span class="sxs-lookup"><span data-stu-id="2759b-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="2759b-106">Utilisez la propriété [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) pour empêcher la mise à jour corrective des privilèges les plus faibles d’une application.</span><span class="sxs-lookup"><span data-stu-id="2759b-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="2759b-107">La stratégie DisableLUAPatching est disponible à partir de Windows Installer version 3,0.</span><span class="sxs-lookup"><span data-stu-id="2759b-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="2759b-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="2759b-108">Registry Key</span></span>

<span data-ttu-id="2759b-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="2759b-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="2759b-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="2759b-110">Data Type</span></span>

<span data-ttu-id="2759b-111">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2759b-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="2759b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2759b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2759b-113">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="2759b-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




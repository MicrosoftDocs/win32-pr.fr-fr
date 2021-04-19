---
description: Cette rubrique décrit les différences entre les versions binaires de la bibliothèque Tablet PC.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Version de la bibliothèque à référencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515226"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="be4af-103">Version de la bibliothèque à référencer</span><span class="sxs-lookup"><span data-stu-id="be4af-103">Which Library Version to Reference</span></span>

<span data-ttu-id="be4af-104">Cette rubrique décrit les différences entre les versions binaires de la bibliothèque Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="be4af-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="be4af-105">Versions de la bibliothèque Tablet PC</span><span class="sxs-lookup"><span data-stu-id="be4af-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="be4af-106">Les fichiers binaires de la bibliothèque Tablet PC (Microsoft.Ink.dll) ont été mis à jour dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be4af-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="be4af-107">Ces fichiers binaires sont appelés « version 6,0 » pour incide avec la version de Windows dans laquelle ils sont publiés.</span><span class="sxs-lookup"><span data-stu-id="be4af-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="be4af-108">La version la plus récente des fichiers binaires qui sont compatibles avec Windows XP est appelée « version 1,7 ».</span><span class="sxs-lookup"><span data-stu-id="be4af-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="be4af-109">Le SDK Windows peut être installé sur les ordinateurs Vista et XP, et le SDK Windows comprend les deux versions de Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="be4af-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="be4af-110">Celles-ci sont installées dans :</span><span class="sxs-lookup"><span data-stu-id="be4af-110">These are installed in:</span></span>

1. <span data-ttu-id="be4af-111">% ProgramFiles% \\ assemblys de référence \\ Microsoft \\ Tablet \\ PC v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="be4af-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="be4af-112">% ProgramFiles% \\ assemblys de référence \\ Microsoft \\ Tablet \\ PC v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="be4af-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="be4af-113">Les fichiers binaires de version 6,0 sont uniquement compatibles avec Windows Vista, et les applications écrites pour eux ne doivent être exécutées que sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be4af-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="be4af-114">Une application écrite avec les binaires de la version 1,7 doit s’exécuter sans modification quand elle est installée sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be4af-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 




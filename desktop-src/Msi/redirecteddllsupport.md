---
description: Le programme d’installation définit la propriété RedirectedDLLSupport si la plateforme système effectuant l’installation prend en charge les composants isolés.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriété RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523643"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="53821-103">Propriété RedirectedDLLSupport</span><span class="sxs-lookup"><span data-stu-id="53821-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="53821-104">Le programme d’installation définit la propriété **RedirectedDLLSupport** si la plateforme système effectuant l’installation prend en charge les [composants isolés](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="53821-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="53821-105">Le programme d’installation affecte à la propriété **RedirectedDLLSupport** la valeur 1 si le système effectuant l’installation prend en charge les [composants isolés](isolated-components.md) basés sur. Fichiers locaux.</span><span class="sxs-lookup"><span data-stu-id="53821-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="53821-106">Le programme d’installation définit la propriété **RedirectedDLLSupport** sur la valeur 2 si le système qui exécute l’installation prend en charge l’isolation à l’aide de l’une ou l’autre. Des fichiers locaux ou des assemblys Win32 côte à côte.</span><span class="sxs-lookup"><span data-stu-id="53821-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="53821-107">La propriété **RedirectedDLLSupport** peut être utilisée pour conditionner l' [action IsolateComponents](isolatecomponents-action.md) dans la [table InstallUISequence](installuisequence-table.md) ou la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="53821-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53821-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53821-108">Requirements</span></span>



| <span data-ttu-id="53821-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53821-109">Requirement</span></span> | <span data-ttu-id="53821-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="53821-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53821-111">Version</span><span class="sxs-lookup"><span data-stu-id="53821-111">Version</span></span><br/> | <span data-ttu-id="53821-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="53821-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="53821-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="53821-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="53821-114">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53821-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="53821-115">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="53821-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53821-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53821-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53821-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53821-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





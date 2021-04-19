---
description: La propriété MsiNetAssemblySupport indique si l’ordinateur prend en charge les assemblys Common Language Runtime.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propriété MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520865"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="e78fc-103">Propriété MsiNetAssemblySupport</span><span class="sxs-lookup"><span data-stu-id="e78fc-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="e78fc-104">La propriété **MsiNetAssemblySupport** indique si l’ordinateur prend en charge les assemblys Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="e78fc-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="e78fc-105">Sur les systèmes qui prennent en charge les assemblys CLR (Common Language Runtime), le programme d’installation définit la valeur de **MsiNetAssemblySupport** sur la version de fichier de Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="e78fc-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="e78fc-106">Le programme d’installation ne définit pas cette propriété si le système d’exploitation ne prend pas en charge les assemblys Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="e78fc-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="e78fc-107">Lorsque plusieurs versions de Fusion.dll sont installées côte à côte sur l’ordinateur de l’utilisateur, cette propriété est définie sur la version la plus récente du fichier Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="e78fc-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="e78fc-108">Par exemple, si .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15) et .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) sont installés côte à côte, la propriété **MsiNetAssemblySupport** est définie sur 1.1.4322.314.</span><span class="sxs-lookup"><span data-stu-id="e78fc-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="e78fc-109">Pour plus d’informations, consultez [assemblys](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="e78fc-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e78fc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e78fc-110">Requirements</span></span>



| <span data-ttu-id="e78fc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e78fc-111">Requirement</span></span> | <span data-ttu-id="e78fc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e78fc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78fc-113">Version</span><span class="sxs-lookup"><span data-stu-id="e78fc-113">Version</span></span><br/> | <span data-ttu-id="e78fc-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e78fc-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e78fc-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e78fc-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e78fc-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e78fc-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e78fc-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e78fc-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e78fc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e78fc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78fc-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e78fc-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





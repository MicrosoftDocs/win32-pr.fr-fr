---
description: Le programme d’installation définit la propriété SystemFolder sur le chemin d’accès complet du dossier système.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propriété SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540558"
---
# <a name="systemfolder-property"></a><span data-ttu-id="b7060-103">Propriété SystemFolder</span><span class="sxs-lookup"><span data-stu-id="b7060-103">SystemFolder property</span></span>

<span data-ttu-id="b7060-104">Le programme d’installation définit la propriété **SystemFolder** sur le chemin d’accès complet du dossier système.</span><span class="sxs-lookup"><span data-stu-id="b7060-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7060-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b7060-105">Remarks</span></span>

<span data-ttu-id="b7060-106">Le programme d’installation définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b7060-106">The installer sets this property.</span></span> <span data-ttu-id="b7060-107">Par exemple, sur Windows 32 bits, la valeur peut être C : \\ Windows \\ system32.</span><span class="sxs-lookup"><span data-stu-id="b7060-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="b7060-108">Sur Windows 64 bits, la valeur peut être C : \\ Windows \\ SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="b7060-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="b7060-109">Ce dossier est normalement un sous-répertoire du dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="b7060-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="b7060-110">Toutefois, il réside sur un serveur lorsqu’il est configuré pour les fenêtres partagées.</span><span class="sxs-lookup"><span data-stu-id="b7060-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="b7060-111">Ce dossier est local, même s’il est configuré pour les fenêtres partagées.</span><span class="sxs-lookup"><span data-stu-id="b7060-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7060-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7060-112">Requirements</span></span>



| <span data-ttu-id="b7060-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7060-113">Requirement</span></span> | <span data-ttu-id="b7060-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7060-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7060-115">Version</span><span class="sxs-lookup"><span data-stu-id="b7060-115">Version</span></span><br/> | <span data-ttu-id="b7060-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7060-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7060-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7060-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7060-118">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7060-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b7060-119">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b7060-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7060-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7060-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7060-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7060-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 





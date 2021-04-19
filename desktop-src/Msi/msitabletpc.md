---
description: Le programme d’installation définit la propriété MsiTabletPC sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP Édition Tablet PC.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriété MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529946"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="6e14f-103">Propriété MsiTabletPC</span><span class="sxs-lookup"><span data-stu-id="6e14f-103">MsiTabletPC property</span></span>

<span data-ttu-id="6e14f-104">Le programme d’installation définit la propriété **MsiTabletPC** sur une valeur différente de zéro si le système d’exploitation actuel est Windows XP Édition Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="6e14f-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="6e14f-105">Le programme d’installation utilise la fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec **SM \_ TABLETPC**, et la propriété reçoit la valeur différente de zéro retournée par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="6e14f-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="6e14f-106">Si le système actuel n’est pas Windows XP Édition Tablet PC, la fonction **GetSystemMetrics** retourne la valeur zéro et le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6e14f-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e14f-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e14f-107">Requirements</span></span>



| <span data-ttu-id="6e14f-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e14f-108">Requirement</span></span> | <span data-ttu-id="6e14f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e14f-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e14f-110">Version</span><span class="sxs-lookup"><span data-stu-id="6e14f-110">Version</span></span><br/> | <span data-ttu-id="6e14f-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e14f-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6e14f-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6e14f-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6e14f-113">Windows Installer 4,5 sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6e14f-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6e14f-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6e14f-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e14f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e14f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e14f-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e14f-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6e14f-117">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6e14f-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

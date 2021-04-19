---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteEnterprise sur 1 si Windows 2000 Advanced Server est installé.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Propriété MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528635"
---
# <a name="msintsuiteenterprise-property"></a><span data-ttu-id="ef2ba-103">Propriété MsiNTSuiteEnterprise</span><span class="sxs-lookup"><span data-stu-id="ef2ba-103">MsiNTSuiteEnterprise property</span></span>

<span data-ttu-id="ef2ba-104">Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteEnterprise** sur 1 si Windows 2000 Advanced Server est installé.</span><span class="sxs-lookup"><span data-stu-id="ef2ba-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteEnterprise** property to 1 if Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="ef2ba-105">Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur de version Enterprise de ver suite est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="ef2ba-105">The installer sets this property to 1 only if the VER\_SUITE\_ENTERPRISE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="ef2ba-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ef2ba-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2ba-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef2ba-107">Requirements</span></span>



| <span data-ttu-id="ef2ba-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef2ba-108">Requirement</span></span> | <span data-ttu-id="ef2ba-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef2ba-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2ba-110">Version</span><span class="sxs-lookup"><span data-stu-id="ef2ba-110">Version</span></span><br/> | <span data-ttu-id="ef2ba-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef2ba-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ef2ba-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ef2ba-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ef2ba-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ef2ba-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ef2ba-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ef2ba-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef2ba-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2ba-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2ba-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef2ba-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

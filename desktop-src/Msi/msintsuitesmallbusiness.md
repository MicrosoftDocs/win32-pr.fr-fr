---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteSmallBusiness sur 1 si Microsoft Small Business Server est installé.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: Propriété MsiNTSuiteSmallBusiness
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8b1e523ff038e4639cb0f92762c3914bbf5f6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544084"
---
# <a name="msintsuitesmallbusiness-property"></a><span data-ttu-id="d66a6-103">Propriété MsiNTSuiteSmallBusiness</span><span class="sxs-lookup"><span data-stu-id="d66a6-103">MsiNTSuiteSmallBusiness property</span></span>

<span data-ttu-id="d66a6-104">Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteSmallBusiness** sur 1 si Microsoft Small Business Server est installé.</span><span class="sxs-lookup"><span data-stu-id="d66a6-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusiness** property to 1 if Microsoft Small Business Server is installed.</span></span> <span data-ttu-id="d66a6-105">Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur SMALLBUSINESS de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="d66a6-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="d66a6-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d66a6-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66a6-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d66a6-107">Requirements</span></span>



| <span data-ttu-id="d66a6-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d66a6-108">Requirement</span></span> | <span data-ttu-id="d66a6-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d66a6-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d66a6-110">Version</span><span class="sxs-lookup"><span data-stu-id="d66a6-110">Version</span></span><br/> | <span data-ttu-id="d66a6-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d66a6-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d66a6-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d66a6-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d66a6-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d66a6-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d66a6-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d66a6-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d66a6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d66a6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66a6-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d66a6-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

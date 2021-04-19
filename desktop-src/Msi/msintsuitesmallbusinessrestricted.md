---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteSmallBusinessRestricted sur 1 si Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propriété MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537468"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a><span data-ttu-id="dfe2c-103">Propriété MsiNTSuiteSmallBusinessRestricted</span><span class="sxs-lookup"><span data-stu-id="dfe2c-103">MsiNTSuiteSmallBusinessRestricted property</span></span>

<span data-ttu-id="dfe2c-104">Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteSmallBusinessRestricted** sur 1 si Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteSmallBusinessRestricted** property to 1 if Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="dfe2c-105">Le programme d’installation définit cette propriété sur 1 uniquement si \_ l' \_ \_ indicateur de restriction SMALLBUSINESS de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="dfe2c-105">The installer sets this property to 1 only if the VER\_SUITE\_SMALLBUSINESS\_RESTRICTED flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="dfe2c-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe2c-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfe2c-107">Requirements</span></span>



| <span data-ttu-id="dfe2c-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfe2c-108">Requirement</span></span> | <span data-ttu-id="dfe2c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfe2c-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe2c-110">Version</span><span class="sxs-lookup"><span data-stu-id="dfe2c-110">Version</span></span><br/> | <span data-ttu-id="dfe2c-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dfe2c-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dfe2c-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dfe2c-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dfe2c-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dfe2c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfe2c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe2c-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dfe2c-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

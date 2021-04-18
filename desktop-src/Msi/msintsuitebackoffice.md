---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteBackOffice sur 1 si les composants Microsoft BackOffice sont installés.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propriété MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528992"
---
# <a name="msintsuitebackoffice-property"></a><span data-ttu-id="a3199-103">Propriété MsiNTSuiteBackOffice</span><span class="sxs-lookup"><span data-stu-id="a3199-103">MsiNTSuiteBackOffice property</span></span>

<span data-ttu-id="a3199-104">Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteBackOffice** sur 1 si les composants Microsoft BackOffice sont installés.</span><span class="sxs-lookup"><span data-stu-id="a3199-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteBackOffice** property to 1 if Microsoft BackOffice components are installed.</span></span> <span data-ttu-id="a3199-105">Le programme d’installation définit cette propriété sur 1 uniquement si \_ l' \_ indicateur BackOffice ver suite est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="a3199-105">The installer sets this property to 1 only if the VER\_SUITE\_BACKOFFICE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="a3199-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a3199-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3199-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3199-107">Requirements</span></span>



| <span data-ttu-id="a3199-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3199-108">Requirement</span></span> | <span data-ttu-id="a3199-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3199-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3199-110">Version</span><span class="sxs-lookup"><span data-stu-id="a3199-110">Version</span></span><br/> | <span data-ttu-id="a3199-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3199-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a3199-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3199-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a3199-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a3199-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a3199-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a3199-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3199-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3199-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3199-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a3199-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

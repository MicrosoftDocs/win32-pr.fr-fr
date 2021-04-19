---
description: Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété MsiNTSuiteWebServer sur 1 si le programme d’installation s’exécute sur une édition Web du serveur Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Propriété MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545438"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="766a3-103">Propriété MsiNTSuiteWebServer</span><span class="sxs-lookup"><span data-stu-id="766a3-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="766a3-104">Sur les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit la propriété **MsiNTSuiteWebServer** sur 1 si le programme d’installation s’exécute sur une édition Web du serveur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="766a3-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="766a3-105">Le programme d’installation définit cette propriété sur 1 uniquement si \_ l' \_ indicateur de panneau de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="766a3-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="766a3-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="766a3-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="766a3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="766a3-107">Remarks</span></span>

<span data-ttu-id="766a3-108">Cette propriété est disponible uniquement avec la version Windows Server 2003 du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="766a3-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="766a3-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="766a3-109">Requirements</span></span>



| <span data-ttu-id="766a3-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="766a3-110">Requirement</span></span> | <span data-ttu-id="766a3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="766a3-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="766a3-112">Version</span><span class="sxs-lookup"><span data-stu-id="766a3-112">Version</span></span><br/> | <span data-ttu-id="766a3-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="766a3-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="766a3-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="766a3-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="766a3-115">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="766a3-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="766a3-116">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="766a3-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="766a3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="766a3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766a3-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="766a3-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="766a3-119">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="766a3-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 

---
description: Sur Windows XP et les systèmes d’exploitation ultérieurs, le programme d’installation définit la propriété MsiNTSuitePersonal sur 1 si le système d’exploitation est Windows XP Édition personnelle.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propriété MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540254"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="89ed7-103">Propriété MsiNTSuitePersonal</span><span class="sxs-lookup"><span data-stu-id="89ed7-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="89ed7-104">Sur Windows XP et les systèmes d’exploitation ultérieurs, le programme d’installation définit la propriété **MsiNTSuitePersonal** sur 1 si le système d’exploitation est Windows XP Édition personnelle.</span><span class="sxs-lookup"><span data-stu-id="89ed7-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="89ed7-105">Le programme d’installation affecte à cette propriété la valeur 1 uniquement si l' \_ \_ indicateur personnel de la suite ver est défini dans la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="89ed7-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="89ed7-106">Dans le cas contraire, le programme d’installation ne définit pas cette propriété.</span><span class="sxs-lookup"><span data-stu-id="89ed7-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ed7-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89ed7-107">Requirements</span></span>



| <span data-ttu-id="89ed7-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89ed7-108">Requirement</span></span> | <span data-ttu-id="89ed7-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="89ed7-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ed7-110">Version</span><span class="sxs-lookup"><span data-stu-id="89ed7-110">Version</span></span><br/> | <span data-ttu-id="89ed7-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89ed7-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="89ed7-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="89ed7-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="89ed7-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89ed7-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="89ed7-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="89ed7-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89ed7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89ed7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ed7-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="89ed7-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

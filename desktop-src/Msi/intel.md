---
description: La propriété Intel est définie par la Windows Installer au niveau du processeur numérique lors de l’exécution sur un processeur Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539936"
---
# <a name="intel-property"></a><span data-ttu-id="d31ea-103">Intel, propriété</span><span class="sxs-lookup"><span data-stu-id="d31ea-103">Intel property</span></span>

<span data-ttu-id="d31ea-104">La propriété **Intel** est définie par la Windows Installer au niveau du processeur numérique lors de l’exécution sur un processeur Intel.</span><span class="sxs-lookup"><span data-stu-id="d31ea-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="d31ea-105">Les valeurs sont les mêmes que celles du champ *wProcessorLevel* de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="d31ea-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="d31ea-106">Lors de l’exécution sur un processeur x64, le Windows Installer définit la propriété **Intel** pour refléter le processeur x86 émulé par l’ordinateur x64, comme indiqué par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d31ea-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d31ea-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d31ea-107">Requirements</span></span>



| <span data-ttu-id="d31ea-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d31ea-108">Requirement</span></span> | <span data-ttu-id="d31ea-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d31ea-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d31ea-110">Version</span><span class="sxs-lookup"><span data-stu-id="d31ea-110">Version</span></span><br/> | <span data-ttu-id="d31ea-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d31ea-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d31ea-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d31ea-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d31ea-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d31ea-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d31ea-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d31ea-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d31ea-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d31ea-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31ea-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d31ea-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 

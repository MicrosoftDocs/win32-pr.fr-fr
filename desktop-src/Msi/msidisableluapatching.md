---
description: Affectez la valeur 1 à la propriété MSIDISABLELUAPATCHING sur la ligne de commande ou dans la table de propriétés pour empêcher la mise à jour corrective de moindre privilège d’une application.
ms.assetid: bf6b8794-332e-4069-8d6f-6d8dc9b01866
title: Propriété MSIDISABLELUAPATCHING
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15bbb8831ad3cff430bf86aee8a17f0ddeace7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523662"
---
# <a name="msidisableluapatching-property"></a><span data-ttu-id="9b50b-103">Propriété MSIDISABLELUAPATCHING</span><span class="sxs-lookup"><span data-stu-id="9b50b-103">MSIDISABLELUAPATCHING property</span></span>

<span data-ttu-id="9b50b-104">Affectez la valeur 1 à la propriété **MSIDISABLELUAPATCHING** sur la ligne de commande ou dans la table de [Propriétés](property-table.md) pour empêcher la mise à jour corrective de moindre privilège d’une application.</span><span class="sxs-lookup"><span data-stu-id="9b50b-104">Set the **MSIDISABLELUAPATCHING** property to 1 on the command line or in the [Property](property-table.md) table to prevent least-privilege patching of an application.</span></span> <span data-ttu-id="9b50b-105">Pour empêcher la mise à jour corrective des privilèges minimum de toutes les applications sur l’ordinateur, définissez la stratégie [DisableLUAPatching](disableluapatching.md) sur 1.</span><span class="sxs-lookup"><span data-stu-id="9b50b-105">To prevent least-privilege patching of all applications on the computer, set the [DisableLUAPatching](disableluapatching.md) policy to 1.</span></span> <span data-ttu-id="9b50b-106">Pour plus d’informations sur la mise à jour corrective des comptes d’utilisateur avec privilèges minimum, consultez Mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="9b50b-106">For information about least-privilege user account patching, see [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b50b-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b50b-107">Requirements</span></span>



| <span data-ttu-id="9b50b-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b50b-108">Requirement</span></span> | <span data-ttu-id="9b50b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b50b-109">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b50b-110">Version</span><span class="sxs-lookup"><span data-stu-id="9b50b-110">Version</span></span><br/> | <span data-ttu-id="9b50b-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b50b-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9b50b-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b50b-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9b50b-113">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9b50b-113">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9b50b-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9b50b-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b50b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b50b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b50b-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9b50b-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9b50b-117">Mise à jour corrective du contrôle de compte d’utilisateur (UAC)</span><span class="sxs-lookup"><span data-stu-id="9b50b-117">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="9b50b-118">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="9b50b-118">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="9b50b-119">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="9b50b-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





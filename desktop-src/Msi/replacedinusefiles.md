---
description: La propriété ReplacedInUseFiles est définie si le programme d’installation écrit sur un fichier qui est en cours d’utilisation.
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: Propriété ReplacedInUseFiles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541589"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="78454-103">Propriété ReplacedInUseFiles</span><span class="sxs-lookup"><span data-stu-id="78454-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="78454-104">La propriété **ReplacedInUseFiles** est définie si le programme d’installation écrit sur un fichier qui est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="78454-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="78454-105">Cette propriété est utilisée par les actions personnalisées pour détecter qu’un redémarrage est nécessaire pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="78454-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="78454-106">Défini pendant les actions [InstallExecute](installexecute-action.md) et [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="78454-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="78454-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78454-107">Requirements</span></span>



| <span data-ttu-id="78454-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78454-108">Requirement</span></span> | <span data-ttu-id="78454-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="78454-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78454-110">Version</span><span class="sxs-lookup"><span data-stu-id="78454-110">Version</span></span><br/> | <span data-ttu-id="78454-111">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78454-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78454-112">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78454-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78454-113">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78454-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="78454-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="78454-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78454-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78454-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78454-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="78454-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 





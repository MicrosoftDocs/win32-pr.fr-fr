---
description: Le programme d’installation définit la valeur de la propriété MsiRestartManagerSessionKey sur la clé de session pour la session du gestionnaire de redémarrage.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propriété MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526382"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="1eed7-103">Propriété MsiRestartManagerSessionKey</span><span class="sxs-lookup"><span data-stu-id="1eed7-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="1eed7-104">Le programme d’installation définit la valeur de la propriété **MsiRestartManagerSessionKey** sur la clé de session pour la session du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1eed7-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="1eed7-105">Les actions personnalisées peuvent utiliser la clé de session pour rejoindre la session du [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1eed7-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eed7-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1eed7-106">Remarks</span></span>

<span data-ttu-id="1eed7-107">Le programme d’installation définit la valeur de la propriété **MsiRestartManagerSessionKey** lors de l’initialisation, puis efface la valeur lors de l’action [InstallValidate](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="1eed7-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="1eed7-108">Les actions personnalisées qui ont besoin de la valeur de la propriété **MsiRestartManagerSessionKey** doivent être prévenues de l’action InstallValidate dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="1eed7-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eed7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eed7-109">Requirements</span></span>



| <span data-ttu-id="1eed7-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eed7-110">Requirement</span></span> | <span data-ttu-id="1eed7-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eed7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eed7-112">Version</span><span class="sxs-lookup"><span data-stu-id="1eed7-112">Version</span></span><br/> | <span data-ttu-id="1eed7-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1eed7-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1eed7-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1eed7-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1eed7-115">Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1eed7-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1eed7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eed7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eed7-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1eed7-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1eed7-118">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="1eed7-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

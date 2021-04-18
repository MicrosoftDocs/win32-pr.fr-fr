---
description: Le programme d’installation définit la propriété WindowsVolume sur le volume du dossier Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propriété WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540309"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="1068e-103">Propriété WindowsVolume</span><span class="sxs-lookup"><span data-stu-id="1068e-103">WindowsVolume property</span></span>

<span data-ttu-id="1068e-104">Le programme d’installation définit la propriété **WindowsVolume** sur le volume du dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="1068e-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="1068e-105">La propriété se termine toujours par une barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="1068e-105">The property always ends with a backslash.</span></span> <span data-ttu-id="1068e-106">Cela peut être utilisé pour définir l’emplacement par défaut sur le volume sur lequel se trouve le dossier Windows, car la propriété [**ROOTDRIVE**](rootdrive.md) n’est pas nécessairement égale à ce lecteur.</span><span class="sxs-lookup"><span data-stu-id="1068e-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="1068e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1068e-107">Remarks</span></span>

<span data-ttu-id="1068e-108">N’utilisez pas la propriété **WindowsVolume** dans la colonne Directory de la table [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1068e-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="1068e-109">La propriété [**WindowsFolder**](windowsfolder.md) contient le chemin d’accès au dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="1068e-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="1068e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1068e-110">Requirements</span></span>



| <span data-ttu-id="1068e-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1068e-111">Requirement</span></span> | <span data-ttu-id="1068e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1068e-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1068e-113">Version</span><span class="sxs-lookup"><span data-stu-id="1068e-113">Version</span></span><br/> | <span data-ttu-id="1068e-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1068e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1068e-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1068e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1068e-116">Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1068e-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1068e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1068e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1068e-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1068e-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 





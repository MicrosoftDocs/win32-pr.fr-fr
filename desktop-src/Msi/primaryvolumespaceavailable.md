---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceAvailable sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriété PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525242"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="3218f-103">Propriété PrimaryVolumeSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="3218f-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="3218f-104">Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceAvailable** sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="3218f-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="3218f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3218f-105">Remarks</span></span>

<span data-ttu-id="3218f-106">Par exemple, si [**PrimaryVolumePath**](primaryvolumepath.md) est défini sur « D : » et que le volume D : a 446 134 272 octets libres, **PrimaryVolumeSpaceAvailable** est défini sur 871356.</span><span class="sxs-lookup"><span data-stu-id="3218f-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="3218f-107">Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.</span><span class="sxs-lookup"><span data-stu-id="3218f-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="3218f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3218f-108">Requirements</span></span>



| <span data-ttu-id="3218f-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3218f-109">Requirement</span></span> | <span data-ttu-id="3218f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3218f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3218f-111">Version</span><span class="sxs-lookup"><span data-stu-id="3218f-111">Version</span></span><br/> | <span data-ttu-id="3218f-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3218f-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3218f-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3218f-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3218f-114">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3218f-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3218f-115">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3218f-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3218f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3218f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3218f-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3218f-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





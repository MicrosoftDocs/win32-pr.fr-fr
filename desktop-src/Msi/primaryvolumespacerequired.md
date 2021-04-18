---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRequired sur une chaîne représentant le nombre total d’octets requis par toutes les fonctionnalités sélectionnées sur le volume référencé par la propriété PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propriété PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529022"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="2584c-103">Propriété PrimaryVolumeSpaceRequired</span><span class="sxs-lookup"><span data-stu-id="2584c-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="2584c-104">Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceRequired** sur une chaîne représentant le nombre total d’octets requis par toutes les fonctionnalités sélectionnées sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="2584c-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="2584c-105">Comme avec la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , ce nombre est exprimé en unités de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="2584c-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="2584c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2584c-106">Remarks</span></span>

<span data-ttu-id="2584c-107">Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.</span><span class="sxs-lookup"><span data-stu-id="2584c-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2584c-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2584c-108">Requirements</span></span>



| <span data-ttu-id="2584c-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2584c-109">Requirement</span></span> | <span data-ttu-id="2584c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2584c-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2584c-111">Version</span><span class="sxs-lookup"><span data-stu-id="2584c-111">Version</span></span><br/> | <span data-ttu-id="2584c-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2584c-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2584c-113">Windows Installer 4,0 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2584c-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2584c-114">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2584c-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2584c-115">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2584c-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2584c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2584c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2584c-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2584c-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





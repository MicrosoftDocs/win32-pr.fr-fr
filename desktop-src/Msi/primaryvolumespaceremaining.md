---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRemaining sur une chaîne représentant le nombre total d’octets restants sur le volume référencé par la propriété PrimaryVolumePath, si toutes les fonctionnalités actuellement sélectionnées ont été installées.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propriété PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535417"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="4af97-103">Propriété PrimaryVolumeSpaceRemaining</span><span class="sxs-lookup"><span data-stu-id="4af97-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="4af97-104">Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceRemaining** sur une chaîne représentant le nombre total d’octets restants sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) , si toutes les fonctionnalités actuellement sélectionnées ont été installées.</span><span class="sxs-lookup"><span data-stu-id="4af97-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="4af97-105">Comme avec la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , ce nombre est exprimé en unités de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="4af97-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af97-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4af97-106">Remarks</span></span>

<span data-ttu-id="4af97-107">Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.</span><span class="sxs-lookup"><span data-stu-id="4af97-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4af97-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4af97-108">Requirements</span></span>



| <span data-ttu-id="4af97-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4af97-109">Requirement</span></span> | <span data-ttu-id="4af97-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4af97-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4af97-111">Version</span><span class="sxs-lookup"><span data-stu-id="4af97-111">Version</span></span><br/> | <span data-ttu-id="4af97-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4af97-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4af97-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4af97-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4af97-114">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="4af97-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4af97-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4af97-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af97-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4af97-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 





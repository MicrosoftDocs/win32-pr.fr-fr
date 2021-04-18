---
description: La définition de cette propriété est semblable à la définition de la stratégie de stratégie TransformsAtSource, à ceci près que l’étendue est différente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propriété TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526673"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="e3344-103">Propriété TRANSFORMSATSOURCE</span><span class="sxs-lookup"><span data-stu-id="e3344-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="e3344-104">La définition de cette propriété est semblable à la définition de la stratégie de [stratégie TransformsAtSource](transformsatsource-policy.md) , à ceci près que l’étendue est différente.</span><span class="sxs-lookup"><span data-stu-id="e3344-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="e3344-105">La définition de la stratégie TransformsAtSource s’applique à tous les packages installés par un utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="e3344-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="e3344-106">La définition de la propriété **TRANSFORMSATSOURCE** s’applique au package, quels que soient les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e3344-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3344-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e3344-107">Remarks</span></span>

<span data-ttu-id="e3344-108">Windows Installer interprète la propriété **TRANSFORMSATSOURCE** comme s’il s’agissait de la propriété [**TRANSFORMSSECURE**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="e3344-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="e3344-109">Si l’indicateur @ est passé dans la propriété [**TRANSformations**](transforms.md) , Windows Installer traite les transformations de la liste comme des [transformations sécurisées à la source](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e3344-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3344-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3344-110">Requirements</span></span>



| <span data-ttu-id="e3344-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3344-111">Requirement</span></span> | <span data-ttu-id="e3344-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3344-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3344-113">Version</span><span class="sxs-lookup"><span data-stu-id="e3344-113">Version</span></span><br/> | <span data-ttu-id="e3344-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e3344-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e3344-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3344-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e3344-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3344-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e3344-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e3344-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3344-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3344-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3344-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3344-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: La propriété PATCHNEWPACKAGECODE met à jour la propriété Résumé du numéro de révision d’une image administrative lors de la mise à jour corrective.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propriété PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540993"
---
# <a name="patchnewpackagecode-property"></a><span data-ttu-id="dd42f-103">Propriété PATCHNEWPACKAGECODE</span><span class="sxs-lookup"><span data-stu-id="dd42f-103">PATCHNEWPACKAGECODE property</span></span>

<span data-ttu-id="dd42f-104">La propriété **PATCHNEWPACKAGECODE** met à jour la propriété [**Résumé du numéro de révision**](revision-number-summary.md) d’une image administrative lors de la mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="dd42f-104">The **PATCHNEWPACKAGECODE** property updates the [**Revision Number Summary**](revision-number-summary.md) property of an administrative image during patching.</span></span> <span data-ttu-id="dd42f-105">Cette propriété est définie uniquement par une transformation dans un fichier. msp.</span><span class="sxs-lookup"><span data-stu-id="dd42f-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="dd42f-106">Le fichier. msp doit inclure une transformation qui ajoute cette propriété à la [table de propriétés](property-table.md) et définit sa valeur.</span><span class="sxs-lookup"><span data-stu-id="dd42f-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="dd42f-107">Le programme d’installation écrit ensuite la valeur de **PATCHNEWPACKAGECODE** dans la propriété **Résumé du numéro de révision** .</span><span class="sxs-lookup"><span data-stu-id="dd42f-107">The installer then writes the value of **PATCHNEWPACKAGECODE** to the **Revision Number Summary** property.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd42f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="dd42f-108">Remarks</span></span>

<span data-ttu-id="dd42f-109">Les propriétés **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)et [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) sont utilisées pour mettre à jour les informations de résumé lorsqu’un correctif est installé sur une image administrative.</span><span class="sxs-lookup"><span data-stu-id="dd42f-109">The **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md), and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd42f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd42f-110">Requirements</span></span>



| <span data-ttu-id="dd42f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd42f-111">Requirement</span></span> | <span data-ttu-id="dd42f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd42f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd42f-113">Version</span><span class="sxs-lookup"><span data-stu-id="dd42f-113">Version</span></span><br/> | <span data-ttu-id="dd42f-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd42f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd42f-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd42f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd42f-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dd42f-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dd42f-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dd42f-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd42f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd42f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd42f-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dd42f-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





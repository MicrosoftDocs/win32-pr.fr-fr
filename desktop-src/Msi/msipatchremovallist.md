---
description: Le programme d’installation définit la valeur de la propriété MsiPatchRemovalList sur une liste des correctifs en cours de suppression lors de l’installation.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propriété MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528052"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="34a37-103">Propriété MsiPatchRemovalList</span><span class="sxs-lookup"><span data-stu-id="34a37-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="34a37-104">Le programme d’installation définit la valeur de la propriété **MsiPatchRemovalList** sur une liste des correctifs en cours de suppression lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="34a37-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="34a37-105">Les correctifs sont représentés dans la liste par leurs GUID de code correctif séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="34a37-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="34a37-106">Les développeurs peuvent utiliser la propriété **MsiPatchRemovalList** pour créer un package Windows Installer ou un correctif qui effectue des [actions personnalisées](custom-actions.md) sur la suppression d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="34a37-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="34a37-107">L’action personnalisée peut être créée dans le package d’installation d’origine, un correctif qui a déjà été appliqué au package ou un correctif logiciel qui ne peut pas être [installé](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="34a37-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="34a37-108">L’action personnalisée peut être conditionnée sur la propriété **MsiPatchRemovalList** dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="34a37-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="34a37-109">Pour plus d’informations sur l’inconditionnel des actions, consultez [utilisation des propriétés dans les instructions conditionnelles](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="34a37-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="34a37-110">L’action personnalisée peut obtenir les GUID des correctifs qui sont supprimés de la valeur de la propriété **MsiPatchRemovalList** .</span><span class="sxs-lookup"><span data-stu-id="34a37-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="34a37-111">L’action personnalisée peut déterminer si l’état d’installation du correctif est appliqué, obsolète ou remplacé en appelant la fonction [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou la propriété [**PatchProperty**](patch-patchproperty.md) de l' [objet patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="34a37-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34a37-112">Notes</span><span class="sxs-lookup"><span data-stu-id="34a37-112">Remarks</span></span>

<span data-ttu-id="34a37-113">Pour plus d’informations sur la suppression des correctifs, consultez [suppression des correctifs](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="34a37-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34a37-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34a37-114">Requirements</span></span>



| <span data-ttu-id="34a37-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34a37-115">Requirement</span></span> | <span data-ttu-id="34a37-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a37-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a37-117">Version</span><span class="sxs-lookup"><span data-stu-id="34a37-117">Version</span></span><br/> | <span data-ttu-id="34a37-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34a37-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34a37-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a37-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34a37-120">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34a37-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="34a37-121">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="34a37-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34a37-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34a37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a37-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="34a37-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="34a37-124">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="34a37-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





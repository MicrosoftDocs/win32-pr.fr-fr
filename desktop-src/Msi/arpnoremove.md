---
description: La définition de la propriété ARPNOREMOVE désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui supprime le produit.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: Propriété ARPNOREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540275"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="2820b-103">Propriété ARPNOREMOVE</span><span class="sxs-lookup"><span data-stu-id="2820b-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="2820b-104">La définition de la propriété **ARPNOREMOVE** désactive la fonctionnalité **Ajout/suppression de programmes** du panneau de **configuration** qui supprime le produit.</span><span class="sxs-lookup"><span data-stu-id="2820b-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="2820b-105">Pour Windows 2000, le bouton **supprimer** du produit est désactivé à partir de l’option **Ajout/suppression de programmes** du **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="2820b-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="2820b-106">Pour les systèmes d’exploitation antérieurs, cela a pour effet de supprimer le produit de la liste des produits installés dans le panneau de **configuration** **Ajout/suppression de programmes** .</span><span class="sxs-lookup"><span data-stu-id="2820b-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="2820b-107">Si la propriété **ARPNOREMOVE** est définie, l' [action RegisterProduct](registerproduct-action.md) écrit la valeur « NoRemove » sous la clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="2820b-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="2820b-108">**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **{*clé de produit*}**</span><span class="sxs-lookup"><span data-stu-id="2820b-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="2820b-109">La définition de la propriété **ARPNOREMOVE** empêche l’écriture de la valeur UninstallString sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="2820b-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="2820b-110">La valeur UnistallString est une ligne de commande pour la suppression du produit, au lieu de la reconfiguration du produit.</span><span class="sxs-lookup"><span data-stu-id="2820b-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="2820b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2820b-111">Remarks</span></span>

<span data-ttu-id="2820b-112">Par exemple, cette propriété peut être définie au cours d’une transformation de personnalisation pour empêcher les utilisateurs de supprimer une personnalisation d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2820b-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="2820b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2820b-113">Requirements</span></span>



| <span data-ttu-id="2820b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2820b-114">Requirement</span></span> | <span data-ttu-id="2820b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2820b-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2820b-116">Version</span><span class="sxs-lookup"><span data-stu-id="2820b-116">Version</span></span><br/> | <span data-ttu-id="2820b-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2820b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2820b-118">Windows Installer 4,0 ou Windows Installer 4,5 ou version ultérieure sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2820b-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="2820b-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2820b-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2820b-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2820b-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2820b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2820b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2820b-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2820b-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: La définition de la propriété ARPNOMODIFY désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui modifie le produit.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Propriété ARPNOMODIFY
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530522"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="65367-103">Propriété ARPNOMODIFY</span><span class="sxs-lookup"><span data-stu-id="65367-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="65367-104">La définition de la propriété **ARPNOMODIFY** désactive la fonctionnalité Ajout/suppression de programmes du panneau de configuration qui modifie le produit.</span><span class="sxs-lookup"><span data-stu-id="65367-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="65367-105">Pour Windows 2000, cela désactive le bouton **modifier** du produit dans **Ajout/suppression de programmes** dans le **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="65367-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="65367-106">Sur les systèmes d’exploitation antérieurs, le fait de cliquer sur le bouton **Ajout/suppression de programmes** désinstalle le produit plutôt que d’entrer dans l’Assistant mode de maintenance.</span><span class="sxs-lookup"><span data-stu-id="65367-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="65367-107">Si la propriété **ARPNOMODIFY** est définie, l' [action RegisterProduct](registerproduct-action.md) écrit la valeur « nomodify » sous la clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="65367-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="65367-108">**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Désinstaller** \\ **{*clé de produit*}**</span><span class="sxs-lookup"><span data-stu-id="65367-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="65367-109">Si la propriété **ARPNOMODIFY** est définie et que la propriété [**ARPNOREMOVE**](arpnoremove.md) n’est pas définie, l’action RegisterProduct écrit également la valeur UninstallString sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="65367-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="65367-110">La valeur UnistallString est une ligne de commande pour la suppression du produit, au lieu de la reconfiguration du produit.</span><span class="sxs-lookup"><span data-stu-id="65367-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="65367-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65367-111">Remarks</span></span>

<span data-ttu-id="65367-112">Sur Windows 2000, le bouton **modifier** du produit est désactivé dans **Ajout/suppression de programmes** du **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="65367-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="65367-113">Cette propriété peut être définie par une transformation de personnalisation pour empêcher les utilisateurs de modifier la personnalisation d’un administrateur via **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="65367-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="65367-114">Cette propriété affecte uniquement **Ajout/suppression de programmes**.</span><span class="sxs-lookup"><span data-stu-id="65367-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65367-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65367-115">Requirements</span></span>



| <span data-ttu-id="65367-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65367-116">Requirement</span></span> | <span data-ttu-id="65367-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="65367-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65367-118">Version</span><span class="sxs-lookup"><span data-stu-id="65367-118">Version</span></span><br/> | <span data-ttu-id="65367-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65367-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="65367-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65367-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="65367-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65367-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="65367-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="65367-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65367-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65367-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65367-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="65367-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="65367-125">Exemple de transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="65367-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 





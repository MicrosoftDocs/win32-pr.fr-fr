---
description: Affectez la valeur 1 à la propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS dans la table de propriétés ou sur une ligne de commande.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540001"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="ebfba-103">Propriété MSIUNINSTALLSUPERSEDEDCOMPONENTS</span><span class="sxs-lookup"><span data-stu-id="ebfba-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="ebfba-104">Affectez la valeur 1 à la propriété **MSIUNINSTALLSUPERSEDEDCOMPONENTS** dans la [table de propriétés](property-table.md) ou sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ebfba-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="ebfba-105">Lorsque cette propriété a la valeur 1, le programme d’installation détermine si les composants de tous les correctifs remplacés sont devenus redondants.</span><span class="sxs-lookup"><span data-stu-id="ebfba-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="ebfba-106">Le programme d’installation peut annuler l’inscription et désinstaller les composants redondants pour empêcher la conservation des composants orphelins sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebfba-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="ebfba-107">La définition de cette propriété affecte les composants de tous les correctifs remplacés.</span><span class="sxs-lookup"><span data-stu-id="ebfba-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="ebfba-108">Pour activer cette fonctionnalité pour des composants uniques, utilisez l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ebfba-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="ebfba-109">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ebfba-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="ebfba-110">Les versions antérieures à Windows Installer 4,5 ignorent la propriété **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .</span><span class="sxs-lookup"><span data-stu-id="ebfba-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfba-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebfba-111">Requirements</span></span>



| <span data-ttu-id="ebfba-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebfba-112">Requirement</span></span> | <span data-ttu-id="ebfba-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebfba-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfba-114">Version</span><span class="sxs-lookup"><span data-stu-id="ebfba-114">Version</span></span><br/> | <span data-ttu-id="ebfba-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ebfba-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ebfba-116">Windows Installer 4,5 ou Windows Installer 4,5 sur Windows Vista, Windows XP, Windows Server 2003 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ebfba-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="ebfba-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ebfba-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebfba-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebfba-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfba-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ebfba-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





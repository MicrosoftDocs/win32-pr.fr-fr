---
description: Pour désactiver l’interface utilisateur incorporée pour l’installation définie dans la table MsiEmbeddedUI, affectez la valeur 1 à la propriété MSIDISABLEEEUI sur la ligne de commande.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Propriété MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535269"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="30a9b-103">Propriété MSIDISABLEEEUI</span><span class="sxs-lookup"><span data-stu-id="30a9b-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="30a9b-104">Pour désactiver l’interface utilisateur incorporée pour l’installation définie dans la [table MsiEmbeddedUI](msiembeddedui-table.md), affectez la valeur 1 à la propriété MSIDISABLEEEUI sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="30a9b-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="30a9b-105">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="30a9b-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="30a9b-106">Les versions antérieures à Windows Installer 4,5 ignorent la propriété MSIDISABLEEEUI.</span><span class="sxs-lookup"><span data-stu-id="30a9b-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a9b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="30a9b-107">Remarks</span></span>

<span data-ttu-id="30a9b-108">Dans une installation de plusieurs packages, un package enfant doit généralement utiliser l’interface utilisateur du package parent et ne pas initialiser sa propre interface utilisateur incorporée.</span><span class="sxs-lookup"><span data-stu-id="30a9b-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="30a9b-109">Si la propriété MSIDISABLEEEUI n’est pas définie dans le package parent, le package enfant utilise l’interface utilisateur incorporée du package parent par défaut et ignore la propriété MSIDISABLEEEUI dans le package enfant.</span><span class="sxs-lookup"><span data-stu-id="30a9b-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="30a9b-110">La propriété MSIDISABLEEEUI désactive l’interface utilisateur incorporée pour un package unique.</span><span class="sxs-lookup"><span data-stu-id="30a9b-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="30a9b-111">Vous pouvez utiliser la stratégie [MsiDisableEmbeddedUI](msidisableembeddedui.md) pour désactiver les interfaces utilisateur incorporées pour tous les packages sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30a9b-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a9b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30a9b-112">Requirements</span></span>



| <span data-ttu-id="30a9b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30a9b-113">Requirement</span></span> | <span data-ttu-id="30a9b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30a9b-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a9b-115">Version</span><span class="sxs-lookup"><span data-stu-id="30a9b-115">Version</span></span><br/> | <span data-ttu-id="30a9b-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30a9b-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30a9b-117">Windows Installer 4,5 sur Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="30a9b-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="30a9b-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="30a9b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30a9b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a9b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a9b-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="30a9b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: La \_ propriété lecteur CCP est définie sur le chemin d’accès racine du volume amovible dans lequel la recherche doit être effectuée par RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: CCP_DRIVE, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526059"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="25ff5-103">\_Propriété du lecteur CCP</span><span class="sxs-lookup"><span data-stu-id="25ff5-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="25ff5-104">La **propriété \_ lecteur CCP** est définie sur le chemin d’accès racine du volume amovible dans lequel la recherche doit être effectuée par [RMCCPSearch](rmccpsearch-action.md).</span><span class="sxs-lookup"><span data-stu-id="25ff5-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="25ff5-105">L’action RMCCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant d’effectuer une installation de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="25ff5-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="25ff5-106">Cette propriété est généralement définie par l’intermédiaire de l’interface utilisateur ou d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="25ff5-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="25ff5-107">Cette propriété doit être définie avant l’exécution de l’action [RMCCPSearch](rmccpsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="25ff5-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ff5-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ff5-108">Requirements</span></span>



| <span data-ttu-id="25ff5-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25ff5-109">Requirement</span></span> | <span data-ttu-id="25ff5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ff5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25ff5-111">Version</span><span class="sxs-lookup"><span data-stu-id="25ff5-111">Version</span></span><br/> | <span data-ttu-id="25ff5-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="25ff5-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="25ff5-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25ff5-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="25ff5-114">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25ff5-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="25ff5-115">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="25ff5-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25ff5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ff5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ff5-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="25ff5-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 





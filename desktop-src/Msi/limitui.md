---
description: Si la propriété LIMITUI est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Propriété LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541001"
---
# <a name="limitui-property"></a><span data-ttu-id="1bd85-103">Propriété LIMITUI</span><span class="sxs-lookup"><span data-stu-id="1bd85-103">LIMITUI property</span></span>

<span data-ttu-id="1bd85-104">Si la propriété **LIMITUI** est définie, le niveau d’interface utilisateur (IU) utilisé lors de l’installation du package est limité au niveau de base.</span><span class="sxs-lookup"><span data-stu-id="1bd85-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="1bd85-105">Cette propriété est requise dans les packages qui n’ont pas d’interface utilisateur créée, mais qui contiennent toujours des tables d’interface utilisateur telles que la [table de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="1bd85-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="1bd85-106">Pour obtenir une description des niveaux de l’interface utilisateur, consultez [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="1bd85-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd85-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1bd85-107">Remarks</span></span>

<span data-ttu-id="1bd85-108">Les packages d’installation contenant la propriété **LIMITUI** doivent également contenir la propriété [**ARPNOMODIFY**](arpnomodify.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd85-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="1bd85-109">Cela est nécessaire pour qu’un utilisateur obtienne le comportement correct à partir de l’utilitaire **Ajout/suppression de programmes** dans le **panneau** de configuration lors de la tentative de configuration d’un produit.</span><span class="sxs-lookup"><span data-stu-id="1bd85-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd85-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bd85-110">Requirements</span></span>



| <span data-ttu-id="1bd85-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bd85-111">Requirement</span></span> | <span data-ttu-id="1bd85-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bd85-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd85-113">Version</span><span class="sxs-lookup"><span data-stu-id="1bd85-113">Version</span></span><br/> | <span data-ttu-id="1bd85-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1bd85-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1bd85-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1bd85-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1bd85-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1bd85-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1bd85-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1bd85-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bd85-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bd85-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd85-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1bd85-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1bd85-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="1bd85-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="1bd85-121">**ARPNOMODIFY**</span><span class="sxs-lookup"><span data-stu-id="1bd85-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 





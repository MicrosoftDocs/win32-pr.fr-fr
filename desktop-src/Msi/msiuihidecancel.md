---
description: Cette propriété de Windows Installer indique que le niveau de l’interface utilisateur interne a été défini pour masquer le bouton Annuler.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propriété MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526381"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="bec29-103">Propriété MsiUIHideCancel</span><span class="sxs-lookup"><span data-stu-id="bec29-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="bec29-104">Le programme d’installation définit la propriété **MsiUIHideCancel** sur 1 lorsque le niveau de l’interface utilisateur interne a été défini pour inclure INSTALLUILEVEL \_ HIDECANCEL avec la fonction [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ou la propriété [UILevel](installer-uilevel.md)de l’objet [**installer**](installer-object.md) ou à l’aide des options de [ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="bec29-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bec29-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bec29-105">Requirements</span></span>



| <span data-ttu-id="bec29-106">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bec29-106">Requirement</span></span> | <span data-ttu-id="bec29-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="bec29-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec29-108">Version</span><span class="sxs-lookup"><span data-stu-id="bec29-108">Version</span></span><br/> | <span data-ttu-id="bec29-109">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bec29-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bec29-110">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bec29-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bec29-111">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bec29-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bec29-112">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bec29-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bec29-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bec29-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bec29-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bec29-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bec29-115">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="bec29-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





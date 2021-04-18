---
description: Définissez la propriété MSINODISABLEMEDIA pour empêcher le programme d’installation de définir la propriété DISABLEMEDIA. La définition de la propriété DISABLEMEDIA empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propriété MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543242"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="8dd93-104">Propriété MSINODISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="8dd93-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="8dd93-105">Définissez la propriété **MSINODISABLEMEDIA** pour empêcher le programme d’installation de définir la propriété [**DISABLEMEDIA**](-disablemedia.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd93-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="8dd93-106">La définition de la propriété **DISABLEMEDIA** empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.</span><span class="sxs-lookup"><span data-stu-id="8dd93-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="8dd93-107">Quand **MSINODISABLEMEDIA** n’est pas défini, le programme d’installation peut ajouter [**DISABLEMEDIA**](-disablemedia.md) au flux de propriétés d’administration lors de l’exécution d’une [installation d’administration](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="8dd93-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="8dd93-108">Cela empêche les utilisateurs qui installent à partir de l’image administrative de s’installer à partir d’un support, tel qu’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="8dd93-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="8dd93-109">Lorsque vous effectuez une installation administrative, le programme d’installation ajoute uniquement [**DISABLEMEDIA**](-disablemedia.md) au flux de propriétés d’administration si la propriété de [**Résumé du nombre de pages**](page-count-summary.md) est inférieure à 150.</span><span class="sxs-lookup"><span data-stu-id="8dd93-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="8dd93-110">Si [**DISABLEMEDIA**](-disablemedia.md) est listé dans la propriété [**AdminProperties**](adminproperties.md) , la définition de **MSINODISABLEMEDIA** empêche la définition de **DISABLEMEDIA** au cours d’une installation d’administration.</span><span class="sxs-lookup"><span data-stu-id="8dd93-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="8dd93-111">Dans ce cas, le programme d’installation peut inscrire une source de média et un utilisateur peut alors avoir la possibilité de réinstaller à partir de la source du média si l’image d’installation d’administration d’origine n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="8dd93-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd93-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dd93-112">Requirements</span></span>



| <span data-ttu-id="8dd93-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dd93-113">Requirement</span></span> | <span data-ttu-id="8dd93-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dd93-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd93-115">Version</span><span class="sxs-lookup"><span data-stu-id="8dd93-115">Version</span></span><br/> | <span data-ttu-id="8dd93-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8dd93-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8dd93-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8dd93-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8dd93-118">Windows Installer sur Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8dd93-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="8dd93-119">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd93-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dd93-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dd93-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd93-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8dd93-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 





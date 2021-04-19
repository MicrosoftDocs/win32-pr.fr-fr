---
description: La définition de la propriété DISABLEMEDIA empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit. Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Propriété DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525244"
---
# <a name="disablemedia-property"></a><span data-ttu-id="bbaa0-104">Propriété DISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="bbaa0-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="bbaa0-105">La définition de la propriété [**DISABLEMEDIA**](disablemedia.md) empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="bbaa0-106">Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbaa0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bbaa0-107">Remarks</span></span>

<span data-ttu-id="bbaa0-108">Notez que la propriété [**DISABLEMEDIA**](disablemedia.md) a un effet différent de la définition de la stratégie DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="bbaa0-109">La définition de **DISABLEMEDIA** empêche l’inscription d’une source de support, ce qui empêche également la première installation d’une application à partir d’une source multimédia.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="bbaa0-110">Pour plus d’informations sur la sécurisation des sources multimédias de l' [*application gérée*](m-gly.md) par rapport à la navigation et l’installation par des utilisateurs non administratifs, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="bbaa0-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbaa0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbaa0-111">Requirements</span></span>



| <span data-ttu-id="bbaa0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbaa0-112">Requirement</span></span> | <span data-ttu-id="bbaa0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbaa0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaa0-114">Version</span><span class="sxs-lookup"><span data-stu-id="bbaa0-114">Version</span></span><br/> | <span data-ttu-id="bbaa0-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbaa0-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbaa0-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bbaa0-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bbaa0-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaa0-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbaa0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbaa0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbaa0-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bbaa0-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 





---
description: 'Si le package d’installation livré avec une application ne se trouve pas à la racine du CD-ROM que les clients reçoivent, la propriété MEDIAPACKAGEPATH doit être définie sur la ligne de commande sur le chemin d’accès relatif de l’application sur le CD-ROM. Par exemple, si le chemin d’accès au package sur le média est E : \\ MyPath \\My.msi, utilisez MEDIAPACKAGEPATH =&\# 0034 ; \\ MyPath \\ & \# 0034 ;. Les administrateurs peuvent créer des CD-ROMs à partir d’un point d’installation d’administration. Si l’emplacement de la racine de l’installation a été modifié sur les nouveaux CD-ROM, la propriété MEDIAPACKAGEPATH doit être définie sur le nouveau chemin d’accès à installer à partir de ce média. Une source avec un emplacement sur le CD-ROM autre que celui spécifié dans le package est inutilisable. Toutefois, il n’est pas nécessaire d’utiliser cette propriété lors de la création d’un point d’installation d’administration à partir de médias d’expédition.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propriété MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542631"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="fc5f6-106">Propriété MEDIAPACKAGEPATH</span><span class="sxs-lookup"><span data-stu-id="fc5f6-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="fc5f6-107">Si le package d’installation livré avec une application ne se trouve pas à la racine du CD-ROM que les clients reçoivent, la propriété **MEDIAPACKAGEPATH** doit être définie sur la ligne de commande sur le chemin d’accès relatif de l’application sur le CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="fc5f6-108">Par exemple, si le chemin d’accès au package sur le média est E : \\ MyPath \\My.msi, utilisez MEDIAPACKAGEPATH = " \\ myPath \\ ".</span><span class="sxs-lookup"><span data-stu-id="fc5f6-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="fc5f6-109">Les administrateurs peuvent créer des CD-ROMs à partir d’un point d’installation d’administration.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="fc5f6-110">Si l’emplacement de la racine de l’installation a été modifié sur les nouveaux CD-ROM, la propriété **MEDIAPACKAGEPATH** doit être définie sur le nouveau chemin d’accès à installer à partir de ce média.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="fc5f6-111">Une source avec un emplacement sur le CD-ROM autre que celui spécifié dans le package est inutilisable.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="fc5f6-112">Toutefois, il n’est pas nécessaire d’utiliser cette propriété lors de la création d’un point d’installation d’administration à partir de médias d’expédition.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5f6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc5f6-113">Requirements</span></span>



| <span data-ttu-id="fc5f6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc5f6-114">Requirement</span></span> | <span data-ttu-id="fc5f6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc5f6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5f6-116">Version</span><span class="sxs-lookup"><span data-stu-id="fc5f6-116">Version</span></span><br/> | <span data-ttu-id="fc5f6-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc5f6-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc5f6-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fc5f6-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5f6-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc5f6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc5f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5f6-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fc5f6-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 





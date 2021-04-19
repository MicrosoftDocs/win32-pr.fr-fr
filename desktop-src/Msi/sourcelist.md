---
description: La propriété SOURCELIST est une liste délimitée par des points-virgules de chemins d’accès source réseau ou URL au package d’installation de l’application.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528625"
---
# <a name="sourcelist-property"></a><span data-ttu-id="8d376-103">SOURCELIST, propriété</span><span class="sxs-lookup"><span data-stu-id="8d376-103">SOURCELIST property</span></span>

<span data-ttu-id="8d376-104">La propriété **SourceList** est une liste délimitée par des points-virgules de chemins d’accès source réseau ou URL au package d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="8d376-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="8d376-105">Cette liste est ajoutée à la fin de la liste source existante de chaque utilisateur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="8d376-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="8d376-106">Le programme d’installation localise une source en énumérant la liste des chemins d’accès source et utilise le premier emplacement accessible trouvé.</span><span class="sxs-lookup"><span data-stu-id="8d376-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="8d376-107">Seule cette source peut être utilisée pour le reste de l’installation.</span><span class="sxs-lookup"><span data-stu-id="8d376-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="8d376-108">Chaque chemin d’accès spécifié dans la liste source doit correspondre à un emplacement disposant d’une source complète pour l’application.</span><span class="sxs-lookup"><span data-stu-id="8d376-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="8d376-109">La totalité de l’arborescence de répertoires à chaque emplacement source doit être la même et doit inclure tous les fichiers sources requis, y compris les armoires.</span><span class="sxs-lookup"><span data-stu-id="8d376-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="8d376-110">Chaque emplacement doit avoir un fichier. msi avec le même nom de fichier et le même code de produit.</span><span class="sxs-lookup"><span data-stu-id="8d376-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="8d376-111">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="8d376-111">Default Value</span></span>

<span data-ttu-id="8d376-112">Le programme d’installation vérifie uniquement la propriété **SourceList** si le produit n’a pas déjà été publié ou installé.</span><span class="sxs-lookup"><span data-stu-id="8d376-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="8d376-113">Dans tous les autres cas, le programme d’installation utilise la liste de sources existante qui se trouve dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8d376-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d376-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8d376-114">Remarks</span></span>

<span data-ttu-id="8d376-115">Les sources ajoutées à l’aide de la propriété **SourceList** sont ajoutées directement à la fin de la liste pour chaque type de source et sont toujours postérieures à la source par défaut spécifiée par la propriété [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="8d376-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="8d376-116">Par Windows Installer le nombre de sources dans la propriété **SourceList** est illimité.</span><span class="sxs-lookup"><span data-stu-id="8d376-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="8d376-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) peut être utilisé pour ajouter des sources réseau.</span><span class="sxs-lookup"><span data-stu-id="8d376-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d376-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d376-118">Requirements</span></span>



| <span data-ttu-id="8d376-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d376-119">Requirement</span></span> | <span data-ttu-id="8d376-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d376-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d376-121">Version</span><span class="sxs-lookup"><span data-stu-id="8d376-121">Version</span></span><br/> | <span data-ttu-id="8d376-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8d376-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8d376-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d376-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8d376-124">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8d376-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8d376-125">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8d376-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d376-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d376-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d376-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d376-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8d376-128">Résilience source</span><span class="sxs-lookup"><span data-stu-id="8d376-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 





---
description: L’Windows Installer définit la propriété OriginalDatabase sur le chemin d’accès de la base de données d’installation utilisée pour lancer l’installation.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propriété OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530516"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="b7ddc-103">Propriété OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="b7ddc-103">OriginalDatabase property</span></span>

<span data-ttu-id="b7ddc-104">L’Windows Installer définit la propriété **OriginalDatabase** sur le chemin d’accès de la base de données d’installation utilisée pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="b7ddc-105">Si l’installation est lancée à partir d’une ligne de commande, la valeur varie selon que l’option de package recache (l’indicateur-v) est présente ou non dans la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ddc-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="b7ddc-106">Méthode d’installation</span><span class="sxs-lookup"><span data-stu-id="b7ddc-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="b7ddc-107">Valeur OriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="b7ddc-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="b7ddc-108">Toute installation lancée en appelant le chemin d’accès du package d’installation (fichier. msi).</span><span class="sxs-lookup"><span data-stu-id="b7ddc-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="b7ddc-109">Chemin d’accès au package d’installation (fichier. msi).</span><span class="sxs-lookup"><span data-stu-id="b7ddc-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="b7ddc-110">Installation lancée à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-110">Installation launched from a command line.</span></span> <span data-ttu-id="b7ddc-111">L’installation n’est pas lancée à partir d’un chemin d’accès au package.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="b7ddc-112">L’option recache (indicateur-v) est présente dans la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ddc-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="b7ddc-113">Chemin d’accès à la base de données sur la source.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="b7ddc-114">Installation lancée à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-114">Installation launched from a command line.</span></span> <span data-ttu-id="b7ddc-115">L’installation n’est pas lancée à partir d’un chemin d’accès au package.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="b7ddc-116">L’option recache (indicateur-v) n’est pas présente dans la propriété [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ddc-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="b7ddc-117">Chemin d’accès à la base de données mise en cache.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="b7ddc-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7ddc-118">Remarks</span></span>

<span data-ttu-id="b7ddc-119">Lors de la première installation, une séquence d’action personnalisée avant l' [action ResolveSource](resolvesource-action.md) peut utiliser la propriété **OriginalDatabase** pour déterminer l’emplacement de la source d’installation.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ddc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7ddc-120">Requirements</span></span>



| <span data-ttu-id="b7ddc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7ddc-121">Requirement</span></span> | <span data-ttu-id="b7ddc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7ddc-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ddc-123">Version</span><span class="sxs-lookup"><span data-stu-id="b7ddc-123">Version</span></span><br/> | <span data-ttu-id="b7ddc-124">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7ddc-125">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7ddc-126">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7ddc-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b7ddc-127">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ddc-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7ddc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7ddc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ddc-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7ddc-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 





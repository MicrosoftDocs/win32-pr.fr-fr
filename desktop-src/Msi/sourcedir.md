---
description: La propriété SourceDir est le répertoire racine qui contient le fichier cab source ou l’arborescence des fichiers sources du package d’installation. Cette valeur est utilisée pour la résolution d’annuaire.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541733"
---
# <a name="sourcedir-property"></a><span data-ttu-id="3a34d-104">SourceDir, propriété</span><span class="sxs-lookup"><span data-stu-id="3a34d-104">SourceDir property</span></span>

<span data-ttu-id="3a34d-105">La propriété **SourceDir** est le répertoire racine qui contient le fichier cab source ou l’arborescence des fichiers sources du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="3a34d-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="3a34d-106">Cette valeur est utilisée pour la résolution d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3a34d-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="3a34d-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="3a34d-107">Default Value</span></span>

<span data-ttu-id="3a34d-108">Répertoire qui contient le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="3a34d-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a34d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3a34d-109">Remarks</span></span>

<span data-ttu-id="3a34d-110">L' [action ResolveSource](resolvesource-action.md) doit être appelée avant d’utiliser la propriété **SourceDir** dans une expression ou une tentative de récupération de la valeur de **SourceDir** avec [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="3a34d-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="3a34d-111">L’action ResolveSource ne doit pas être exécutée tant que la source n’est pas disponible, par exemple lors de la désinstallation d’une application, car cela peut entraîner une invite inattendue pour le média source.</span><span class="sxs-lookup"><span data-stu-id="3a34d-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a34d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a34d-112">Requirements</span></span>



| <span data-ttu-id="3a34d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a34d-113">Requirement</span></span> | <span data-ttu-id="3a34d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a34d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a34d-115">Version</span><span class="sxs-lookup"><span data-stu-id="3a34d-115">Version</span></span><br/> | <span data-ttu-id="3a34d-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a34d-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3a34d-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a34d-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3a34d-118">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a34d-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3a34d-119">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3a34d-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a34d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a34d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a34d-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a34d-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 





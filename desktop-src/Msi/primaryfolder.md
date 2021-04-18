---
description: Le PRIMARYFOLDER est une propriété globale qui permet à l’auteur de désigner un dossier principal pour l’installation.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propriété PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532986"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="5b020-103">Propriété PRIMARYFOLDER</span><span class="sxs-lookup"><span data-stu-id="5b020-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="5b020-104">Le **PRIMARYFOLDER** est une propriété globale qui permet à l’auteur de désigner un dossier principal pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5b020-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="5b020-105">La valeur de cette propriété doit être le nom de clé d’un répertoire qui existe dans la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="5b020-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="5b020-106">Le programme d’installation utilise le chemin d’accès résolu du dossier principal pour déterminer le volume à utiliser lors de la définition des valeurs de la propriété [**PrimaryVolumePath**](primaryvolumepath.md) , de la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , de la propriété [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) et de la propriété [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .</span><span class="sxs-lookup"><span data-stu-id="5b020-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="5b020-107">Le programme d’installation fournit les valeurs de ces dernières propriétés aux utilisateurs dans l’interface utilisateur pour les aider à gérer l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="5b020-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="5b020-108">Les auteurs de package courants peuvent sélectionner le plus grand dossier comme dossier principal.</span><span class="sxs-lookup"><span data-stu-id="5b020-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="5b020-109">La valeur de cette propriété doit être le nom de clé d’un enregistrement de répertoire trouvé dans la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="5b020-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b020-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b020-110">Requirements</span></span>



| <span data-ttu-id="5b020-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b020-111">Requirement</span></span> | <span data-ttu-id="5b020-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b020-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b020-113">Version</span><span class="sxs-lookup"><span data-stu-id="5b020-113">Version</span></span><br/> | <span data-ttu-id="5b020-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b020-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b020-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b020-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b020-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b020-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5b020-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5b020-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b020-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b020-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b020-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b020-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





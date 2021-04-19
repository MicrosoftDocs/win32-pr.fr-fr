---
description: La propriété ROOTDRIVE spécifie le lecteur par défaut pour le répertoire de destination de l’installation.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Propriété ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537426"
---
# <a name="rootdrive-property"></a><span data-ttu-id="d7bb2-103">Propriété ROOTDRIVE</span><span class="sxs-lookup"><span data-stu-id="d7bb2-103">ROOTDRIVE property</span></span>

<span data-ttu-id="d7bb2-104">La propriété **ROOTDRIVE** spécifie le lecteur par défaut pour le répertoire de destination de l’installation.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="d7bb2-105">Si la colonne Directory de la [table Directory](directory-table.md) indique le répertoire de destination racine par un nom de propriété qui n’est pas défini, le programme d’installation utilise la valeur de la propriété **ROOTDRIVE** pour résoudre le chemin d’accès au répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="d7bb2-106">Si **ROOTDRIVE** n’est pas défini sur une ligne de commande ou qu’il a été créé dans la [table de propriétés](property-table.md), le programme d’installation définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="d7bb2-107">Au cours d’une [installation d’administration](administrative-installation.md) , le programme d’installation définit **ROOTDRIVE** sur le premier lecteur réseau connecté qu’il trouve dans lequel il est possible d’écrire.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="d7bb2-108">S’il ne s’agit pas d’une installation d’administration, ou si le programme d’installation ne peut pas trouver de lecteurs réseau, le programme d’installation définit **ROOTDRIVE** sur le lecteur local qui peut être écrit avec le plus d’espace libre.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="d7bb2-109">La valeur de cette propriété doit se terminer par' \\ '.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bb2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7bb2-110">Requirements</span></span>



| <span data-ttu-id="d7bb2-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bb2-111">Requirement</span></span> | <span data-ttu-id="d7bb2-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bb2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bb2-113">Version</span><span class="sxs-lookup"><span data-stu-id="d7bb2-113">Version</span></span><br/> | <span data-ttu-id="d7bb2-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d7bb2-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d7bb2-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7bb2-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d7bb2-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bb2-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7bb2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7bb2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bb2-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7bb2-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 





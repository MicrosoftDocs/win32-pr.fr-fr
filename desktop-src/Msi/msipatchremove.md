---
description: La propriété MSIPATCHREMOVE spécifie la liste des correctifs à supprimer durant une installation.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propriété MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528051"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="cd6a5-103">Propriété MSIPATCHREMOVE</span><span class="sxs-lookup"><span data-stu-id="cd6a5-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="cd6a5-104">La propriété **MSIPATCHREMOVE** spécifie la liste des correctifs à supprimer durant une installation.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="cd6a5-105">Les correctifs individuels de la liste sont séparés par des points-virgules et peuvent être représentés par le GUID du code correctif ou par le chemin d’accès complet au correctif.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="cd6a5-106">La fonction [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) et la méthode [**RemovePatches**](installer-removepatches.md) de l’objet [installer](installer-object.md) définissent la propriété **MSIPATCHREMOVE** .</span><span class="sxs-lookup"><span data-stu-id="cd6a5-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="cd6a5-107">La propriété **MSIPATCHREMOVE** peut être définie sur la ligne de commande comme suit pour supprimer un correctif.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="cd6a5-108">**msiexec/i A : \\Example.msi MSIPATCHREMOVE = c : \\ patches \\ qfe1. msp ; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="cd6a5-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="cd6a5-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd6a5-109">Requirements</span></span>



| <span data-ttu-id="cd6a5-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd6a5-110">Requirement</span></span> | <span data-ttu-id="cd6a5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd6a5-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6a5-112">Version</span><span class="sxs-lookup"><span data-stu-id="cd6a5-112">Version</span></span><br/> | <span data-ttu-id="cd6a5-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cd6a5-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cd6a5-115">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd6a5-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cd6a5-116">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cd6a5-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd6a5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd6a5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd6a5-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd6a5-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="cd6a5-119">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="cd6a5-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





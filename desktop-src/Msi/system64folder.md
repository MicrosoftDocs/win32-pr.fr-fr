---
description: Le programme d’installation définit la propriété System64Folder sur le chemin d’accès complet au dossier System64 prédéfini. La propriété System64Folder existante est définie sur le dossier 32 bits correspondant.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriété System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543940"
---
# <a name="system64folder-property"></a><span data-ttu-id="f7fb8-104">Propriété System64Folder</span><span class="sxs-lookup"><span data-stu-id="f7fb8-104">System64Folder property</span></span>

<span data-ttu-id="f7fb8-105">Le programme d’installation définit la propriété **System64Folder** sur le chemin d’accès complet au dossier System64 prédéfini.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="f7fb8-106">La propriété **System64Folder** existante est définie sur le dossier 32 bits correspondant.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7fb8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f7fb8-107">Remarks</span></span>

<span data-ttu-id="f7fb8-108">Le programme d’installation définit cette propriété sur Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="f7fb8-109">Par exemple, sur Windows 64 bits, la valeur peut être C : \\ Window \\ system32.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="f7fb8-110">Cette propriété n’est pas utilisée sur Windows 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="f7fb8-111">Ce dossier est normalement un sous-répertoire du dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="f7fb8-112">Toutefois, il réside sur un serveur lorsqu’il est configuré pour les fenêtres partagées.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7fb8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7fb8-113">Requirements</span></span>



| <span data-ttu-id="f7fb8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7fb8-114">Requirement</span></span> | <span data-ttu-id="f7fb8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7fb8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fb8-116">Version</span><span class="sxs-lookup"><span data-stu-id="f7fb8-116">Version</span></span><br/> | <span data-ttu-id="f7fb8-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f7fb8-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f7fb8-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7fb8-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f7fb8-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f7fb8-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7fb8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7fb8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7fb8-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7fb8-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 





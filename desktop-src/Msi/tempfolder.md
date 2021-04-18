---
description: Le programme d’installation définit la propriété TempFolder sur le chemin d’accès complet au dossier Temp. Les auteurs n’ont pas besoin de définir la propriété TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propriété TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532927"
---
# <a name="tempfolder-property"></a><span data-ttu-id="e2eef-103">Propriété TempFolder</span><span class="sxs-lookup"><span data-stu-id="e2eef-103">TempFolder property</span></span>

<span data-ttu-id="e2eef-104">Le programme d’installation définit la propriété **TempFolder** sur le chemin d’accès complet au dossier Temp.</span><span class="sxs-lookup"><span data-stu-id="e2eef-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="e2eef-105">Les auteurs n’ont pas besoin de définir la propriété **TempFolder** .</span><span class="sxs-lookup"><span data-stu-id="e2eef-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="e2eef-106">Windows Installer utilise la fonction [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) pour récupérer le chemin d’accès du répertoire désigné pour les fichiers temporaires et pour définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="e2eef-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2eef-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e2eef-107">Remarks</span></span>

<span data-ttu-id="e2eef-108">La valeur courante de cette propriété est C : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="e2eef-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2eef-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2eef-109">Requirements</span></span>



| <span data-ttu-id="e2eef-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2eef-110">Requirement</span></span> | <span data-ttu-id="e2eef-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2eef-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2eef-112">Version</span><span class="sxs-lookup"><span data-stu-id="e2eef-112">Version</span></span><br/> | <span data-ttu-id="e2eef-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2eef-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2eef-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2eef-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2eef-115">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2eef-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e2eef-116">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e2eef-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2eef-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2eef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2eef-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2eef-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 

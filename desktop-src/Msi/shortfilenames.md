---
description: La définition de la propriété SHORTFILENAMES entraîne l’utilisation de noms de fichiers courts pour les noms de fichiers cibles, plutôt que pour les noms de fichiers longs. Elle n’affecte pas les noms de fichiers que le programme d’installation recherche à la source.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Propriété SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541776"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="1c2a4-104">Propriété SHORTFILENAMES</span><span class="sxs-lookup"><span data-stu-id="1c2a4-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="1c2a4-105">La définition de la propriété **SHORTFILENAMES** entraîne l’utilisation de noms de fichiers courts pour les noms de fichiers cibles, plutôt que pour les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="1c2a4-106">Elle n’affecte pas les noms de fichiers que le programme d’installation recherche à la source.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="1c2a4-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="1c2a4-107">Default Value</span></span>

<span data-ttu-id="1c2a4-108">Les noms longs sont utilisés par le programme d’installation si la propriété **SHORTFILENAMES** n’est pas définie et que le volume cible prend en charge les noms longs.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="1c2a4-109">Les noms courts sont utilisés par le programme d’installation si le volume cible ne prend pas en charge les noms longs.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2a4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1c2a4-110">Remarks</span></span>

<span data-ttu-id="1c2a4-111">Lorsque la propriété **SHORTFILENAMES** est définie, le programme d’installation crée des dossiers et installe les fichiers à l’aide de noms de fichiers courts à partir de toute \| paire de caractères courts figurant dans la table de [fichiers](file-table.md) ou le [tableau de répertoire](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="1c2a4-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="1c2a4-112">Les applications peuvent utiliser la fonction [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) pour récupérer la forme abrégée d’un chemin d’accès de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2a4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c2a4-113">Requirements</span></span>



| <span data-ttu-id="1c2a4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c2a4-114">Requirement</span></span> | <span data-ttu-id="1c2a4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c2a4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2a4-116">Version</span><span class="sxs-lookup"><span data-stu-id="1c2a4-116">Version</span></span><br/> | <span data-ttu-id="1c2a4-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1c2a4-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1c2a4-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c2a4-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1c2a4-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1c2a4-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c2a4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c2a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2a4-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c2a4-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 

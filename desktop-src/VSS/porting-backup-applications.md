---
description: Les fichiers binaires de Windows Server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008. Toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portage des applications de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528708"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="a1e74-104">Portage des applications de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="a1e74-104">Porting Backup Applications</span></span>

<span data-ttu-id="a1e74-105">Les fichiers binaires de Windows Server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a1e74-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a1e74-106">Toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.</span><span class="sxs-lookup"><span data-stu-id="a1e74-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="a1e74-107">Portage des applications de sauvegarde Windows XP vers Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e74-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="a1e74-108">Plusieurs interfaces VSS ont été modifiées depuis Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1e74-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="a1e74-109">Au minimum, les applications Windows XP doivent être recompilées à l’aide de fichiers d’en-tête et de bibliothèques du kit de développement logiciel (SDK) VSS 7,2 ou du kit de développement logiciel (SDK) Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a1e74-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="a1e74-110">Portage des applications de sauvegarde Windows Server 2003 SP1 vers Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e74-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="a1e74-111">Les fichiers binaires de Windows Server 2003 avec SP1 sont compatibles avec Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a1e74-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a1e74-112">Toutefois, la plupart des applications de sauvegarde Windows Server 2003 avec SP1 doivent être mises à jour pour prendre en compte les nouvelles fonctionnalités, qui sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1e74-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="a1e74-113">Compilation d’applications de sauvegarde pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e74-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="a1e74-114">Les applications qui utilisent des interfaces disponibles dans Windows Server 2003 peuvent être compilées à l’aide de fichiers d’en-tête et de bibliothèques fournis dans le kit de développement logiciel (SDK) VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="a1e74-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="a1e74-115">Pour utiliser les nouvelles interfaces, les applications doivent être recompilées à l’aide des fichiers d’en-tête et des bibliothèques inclus dans le kit de développement logiciel (SDK) Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a1e74-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="a1e74-116">Les fichiers binaires compilés à l’aide de Windows Vista ou Windows Server 2008 ne sont pas compatibles avec Windows Server 2003 avec SP1 ou des versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1e74-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 




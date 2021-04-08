---
description: Décrit les opérations de point d’analyse que vous pouvez effectuer à l’aide de DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Opérations de point d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035022"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="98bba-103">Opérations de point d’analyse</span><span class="sxs-lookup"><span data-stu-id="98bba-103">Reparse Point Operations</span></span>

<span data-ttu-id="98bba-104">Pour déterminer si un système de fichiers prend en charge les points d’analyse, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez le **fichier \_ prend en charge \_ \_** l’indicateur de bit points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="98bba-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="98bba-105">La fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) vous permet de définir, de modifier, d’obtenir et de supprimer des points d’analyse.</span><span class="sxs-lookup"><span data-stu-id="98bba-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="98bba-106">Le tableau suivant décrit les opérations de point d’analyse que vous pouvez effectuer à l’aide de **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="98bba-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="98bba-107">Opération</span><span class="sxs-lookup"><span data-stu-id="98bba-107">Operation</span></span>                                                           | <span data-ttu-id="98bba-108">Description</span><span class="sxs-lookup"><span data-stu-id="98bba-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98bba-109">**FSCTL \_ définir le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="98bba-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="98bba-110">Autorise le programme appelant à définir un nouveau point d’analyse ou à en modifier un existant.</span><span class="sxs-lookup"><span data-stu-id="98bba-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="98bba-111">**FSCTL \_ recevoir le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="98bba-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="98bba-112">Obtient les informations stockées dans un point d’analyse existant.</span><span class="sxs-lookup"><span data-stu-id="98bba-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="98bba-113">**FSCTL \_ supprimer le \_ point d’analyse \_**</span><span class="sxs-lookup"><span data-stu-id="98bba-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="98bba-114">Supprime un point d’analyse existant.</span><span class="sxs-lookup"><span data-stu-id="98bba-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="98bba-115">Si vous modifiez, obtenez ou supprimez un point d’analyse, vous devez spécifier la même balise d’analyse dans l’opération qui est contenue dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="98bba-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="98bba-116">Dans le cas contraire, l’opération échouera avec l’erreur erreur d’analyse de la **\_ \_ balise \_ d’analyse**.</span><span class="sxs-lookup"><span data-stu-id="98bba-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="98bba-117">Si vous modifiez ou supprimez un point d’analyse, vous devez également spécifier le **GUID** d’analyse dans l’opération contenue dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="98bba-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="98bba-118">Dans le cas contraire, l’opération échoue avec **le \_ conflit d' \_ attribut \_** d’erreur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="98bba-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="98bba-119">Pour déterminer si un fichier ou un répertoire contient un point d’analyse, utilisez la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="98bba-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="98bba-120">Si le fichier ou le répertoire est associé à un point d’analyse, l’attribut de **\_ point d' \_ analyse \_** de l’attribut de fichier est défini.</span><span class="sxs-lookup"><span data-stu-id="98bba-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="98bba-121">Pour remplacer un point d’analyse existant sans avoir déjà un handle vers le fichier ou le répertoire, appelez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l' **indicateur de fichier \_ ouvrir le \_ \_ \_ point d’analyse**.</span><span class="sxs-lookup"><span data-stu-id="98bba-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="98bba-122">Cet indicateur vous permet d’ouvrir le fichier que le filtre de système de fichiers correspondant soit installé et qu’il fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="98bba-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 


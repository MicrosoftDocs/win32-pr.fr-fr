---
description: Chaque fichier et répertoire sur un volume qui prend en charge la compression de fichiers et de répertoires individuels a un état de compression.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: État de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203089"
---
# <a name="compression-state"></a><span data-ttu-id="e9a33-103">État de compression</span><span class="sxs-lookup"><span data-stu-id="e9a33-103">Compression State</span></span>

<span data-ttu-id="e9a33-104">Chaque fichier et répertoire sur un volume qui prend en charge la compression de fichiers et de répertoires individuels a un *État de compression*.</span><span class="sxs-lookup"><span data-stu-id="e9a33-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="e9a33-105">Tandis que l’attribut de compression d’un fichier ou d’un répertoire indique simplement si le fichier ou le répertoire est compressé ou non compressé, l’état de compression spécifie également le format des données compressées.</span><span class="sxs-lookup"><span data-stu-id="e9a33-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="e9a33-106">Utilisez le code de contrôle [**FSCTL \_ obtenir la \_ compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) pour déterminer l’état de compression d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e9a33-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="e9a33-107">L’état de compression est encodé sous la forme d’une valeur de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e9a33-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="e9a33-108">Une valeur d’état de compression du format de COMPRESSION \_ \_ aucun indique qu’un fichier n’est pas compressé.</span><span class="sxs-lookup"><span data-stu-id="e9a33-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="e9a33-109">\_La valeur par défaut du format de compression \_ indique qu’un fichier est compressé, en utilisant le format de compression par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9a33-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="e9a33-110">Toute autre valeur indique qu’un fichier est compressé, en utilisant le format de compression spécifié par la valeur d’état de compression.</span><span class="sxs-lookup"><span data-stu-id="e9a33-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="e9a33-111">Utilisez le code de contrôle de [**\_ \_ compression Set FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) pour définir l’état de compression d’un fichier ou d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="e9a33-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="e9a33-112">Cette opération définit également l’attribut de compression du fichier ou du répertoire.</span><span class="sxs-lookup"><span data-stu-id="e9a33-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="e9a33-113">La définition de l’état de compression d’un fichier sur une valeur différente de zéro compresse le fichier, en utilisant le format de compression encodé à l’aide de la valeur d’état de compression.</span><span class="sxs-lookup"><span data-stu-id="e9a33-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="e9a33-114">La définition de l’état de compression d’un fichier sur zéro décompresse le fichier.</span><span class="sxs-lookup"><span data-stu-id="e9a33-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="e9a33-115">Il s’agit d’opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="e9a33-115">These are synchronous operations.</span></span> <span data-ttu-id="e9a33-116">Le fichier est compressé ou décompressé immédiatement lorsque vous définissez son état de compression.</span><span class="sxs-lookup"><span data-stu-id="e9a33-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="e9a33-117">La définition de l’état de compression d’un répertoire n’entraîne pas de compression ou de décompression immédiate.</span><span class="sxs-lookup"><span data-stu-id="e9a33-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="e9a33-118">Au lieu de cela, la définition de l’état de compression d’un répertoire définit un état de compression par défaut qui sera attribué à tous les fichiers et sous-répertoires nouvellement créés.</span><span class="sxs-lookup"><span data-stu-id="e9a33-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 

---
title: Utilisation du presse-papiers avec des fichiers AVI
description: Utilisation du presse-papiers avec des fichiers AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard fonction)
- AVIGetFromClipboard fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673281"
---
# <a name="using-the-clipboard-with-avi-files"></a><span data-ttu-id="63208-105">Utilisation du presse-papiers avec des fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="63208-105">Using the Clipboard with AVI Files</span></span>

<span data-ttu-id="63208-106">Le presse-papiers offre un stockage temporaire et pratique qu’une application peut utiliser pour copier ou transférer des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="63208-106">The clipboard provides convenient, temporary storage that an application can use to copy or transfer AVI files.</span></span> <span data-ttu-id="63208-107">AVIFile comprend des fonctions de presse-papiers que vous pouvez utiliser avec des fichiers de disque ou de mémoire.</span><span class="sxs-lookup"><span data-stu-id="63208-107">AVIFile includes clipboard functions that you can use with disk or memory files.</span></span>

<span data-ttu-id="63208-108">Vous pouvez copier un fichier dans le presse-papiers à l’aide de la fonction [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) .</span><span class="sxs-lookup"><span data-stu-id="63208-108">You can copy a file to the clipboard by using the [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) function.</span></span> <span data-ttu-id="63208-109">Pour écrire un fichier qui se trouve dans le presse-papiers sur la mémoire ou sur le disque, utilisez la fonction [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .</span><span class="sxs-lookup"><span data-stu-id="63208-109">To write a file that is on the clipboard to memory or disk, use the [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) function.</span></span>

<span data-ttu-id="63208-110">Vous pouvez effacer un fichier du presse-papiers à l’aide de la fonction [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) .</span><span class="sxs-lookup"><span data-stu-id="63208-110">You can clear a file from the clipboard by using the [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) function.</span></span> <span data-ttu-id="63208-111">Cette fonction n’efface pas les autres types d’informations, tels que le texte, à partir du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="63208-111">This function does not clear other types of information, such as text, from the clipboard.</span></span> <span data-ttu-id="63208-112">Si vous utilisez les fonctions du presse-papiers dans votre application, effacez le presse-papiers avec **AVIClearClipboard** avant de fermer l’application ou de fermer le fichier dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="63208-112">If you use clipboard functions in your application, clear the clipboard with **AVIClearClipboard** before closing the application or closing the file on the clipboard.</span></span> <span data-ttu-id="63208-113">Vous pouvez appeler **AVIClearClipboard** dans votre application, que **AVIPutFileOnClipboard** ait ou non été utilisé.</span><span class="sxs-lookup"><span data-stu-id="63208-113">You can call **AVIClearClipboard** in your application whether or not **AVIPutFileOnClipboard** has been used.</span></span>

> [!Note]  
> <span data-ttu-id="63208-114">Si votre application copie un fichier dans le presse-papiers et que le fichier contient des données de flux susceptibles de changer, vous pouvez créer un fichier de mémoire de flux clonés à l’aide de la fonction [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="63208-114">If your application copies a file to the clipboard and the file contains stream data that might change, you can create a memory file of cloned streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="63208-115">Vous pouvez ensuite placer le fichier dans le presse-papiers, puis libérer le fichier d’origine sans l’invalider.</span><span class="sxs-lookup"><span data-stu-id="63208-115">You can then place the file on the clipboard and then release the original file without invalidating it.</span></span>

 

 

 





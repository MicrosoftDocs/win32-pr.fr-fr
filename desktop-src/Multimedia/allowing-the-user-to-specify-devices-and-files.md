---
title: Autoriser l’utilisateur à spécifier des appareils et des fichiers
description: Autoriser l’utilisateur à spécifier des appareils et des fichiers
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog macro)
- MCIWndOpen macro)
- MCIWndOpenInterface macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673522"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a><span data-ttu-id="bffcf-106">Autoriser l’utilisateur à spécifier des appareils et des fichiers</span><span class="sxs-lookup"><span data-stu-id="bffcf-106">Allowing the User to Specify Devices and Files</span></span>

<span data-ttu-id="bffcf-107">Vous pouvez associer un appareil ou un fichier à une fenêtre MCIWnd existante à l’aide des macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)et [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) , ainsi que de la fonction [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="bffcf-107">You can associate a device or file with an existing MCIWnd window by using the [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen), and [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macros, and the [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) function.</span></span>

<span data-ttu-id="bffcf-108">Pour permettre à un utilisateur de votre application de sélectionner un fichier à lire, utilisez **MCIWndOpenDialog**.</span><span class="sxs-lookup"><span data-stu-id="bffcf-108">To let a user of your application select a file to play, use **MCIWndOpenDialog**.</span></span> <span data-ttu-id="bffcf-109">Cette macro affiche la boîte de dialogue **ouvrir** (illustrée dans la capture d’écran suivante) pour le choix d’un fichier et associe le fichier sélectionné à la fenêtre MCIWnd actuelle.</span><span class="sxs-lookup"><span data-stu-id="bffcf-109">This macro displays the **Open** dialog box (shown in the following screen shot) for choosing a file and associates the selected file with the current MCIWnd window.</span></span>

![image fenêtre MCIWnd](images/mciwnd3.gif)

<span data-ttu-id="bffcf-111">Vous pouvez permettre à un utilisateur de votre application de sélectionner un fichier à associer à une fenêtre MCIWnd et d’afficher un aperçu de ce fichier à l’aide de [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) et [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span><span class="sxs-lookup"><span data-stu-id="bffcf-111">You can let a user of your application select a file to associate with an MCIWnd window and preview that file by using [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen).</span></span> <span data-ttu-id="bffcf-112">La fonction **GetOpenFileNamePreview** affiche la boîte de dialogue **ouvrir** permettant de choisir un fichier et permet à l’utilisateur d’afficher un aperçu (lecture) de son contenu.</span><span class="sxs-lookup"><span data-stu-id="bffcf-112">The **GetOpenFileNamePreview** function displays the **Open** dialog box for choosing a file and lets the user preview (play) its contents.</span></span> <span data-ttu-id="bffcf-113">Lorsque le nom d’un fichier existant est spécifié dans la boîte de dialogue, **GetOpenFileNamePreview** fournit un petit contrôle pour permettre à l’utilisateur d’afficher un aperçu du contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="bffcf-113">When the name of an existing file is specified in the dialog box, **GetOpenFileNamePreview** provides a small control to let the user preview the contents of the file.</span></span> <span data-ttu-id="bffcf-114">Vous pouvez associer un fichier spécifié, sélectionné avec **GetOpenFileNamePreview** ou spécifié d’une autre manière, avec une fenêtre MCIWnd à l’aide de **MCIWndOpen**.</span><span class="sxs-lookup"><span data-stu-id="bffcf-114">You can associate a specified file, selected with **GetOpenFileNamePreview** or specified in another manner, with an MCIWnd window by using **MCIWndOpen**.</span></span>

<span data-ttu-id="bffcf-115">Vous pouvez également utiliser **MCIWndOpen** pour spécifier un appareil à associer à une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="bffcf-115">You can also use **MCIWndOpen** to specify a device to associate with an MCIWnd window.</span></span> <span data-ttu-id="bffcf-116">Par exemple, vous pouvez utiliser un nom de périphérique, tel que « CDAudio ».</span><span class="sxs-lookup"><span data-stu-id="bffcf-116">For example, you can use a device name, such as "CDAudio".</span></span>

<span data-ttu-id="bffcf-117">Pour associer une fenêtre MCIWnd à une interface de fichier ou une interface de flux de données à des données multimédias, utilisez la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="bffcf-117">To associate an MCIWnd window with a file interface or data-stream interface to multimedia data, use the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span> <span data-ttu-id="bffcf-118">Pour plus d’informations sur les interfaces de fichiers et de flux de données, consultez [fonctions et macros avifile](avifile-functions-and-macros.md).</span><span class="sxs-lookup"><span data-stu-id="bffcf-118">For more information about file and data-stream interfaces, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

> [!Note]  
> <span data-ttu-id="bffcf-119">Avant d’associer un nouveau fichier ou un nouveau périphérique à une fenêtre MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) et [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) Fermez tout appareil actuellement associé à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bffcf-119">Before associating a new file or device with an MCIWnd window, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) and [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) close any device currently associated with the window.</span></span> <span data-ttu-id="bffcf-120">Votre application n’a pas besoin de fermer les appareils ouverts avant d’utiliser ces macros.</span><span class="sxs-lookup"><span data-stu-id="bffcf-120">Your application does not need to close any open devices before using these macros.</span></span>

 

 

 





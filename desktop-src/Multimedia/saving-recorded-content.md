---
title: Enregistrement du contenu enregistré
description: Enregistrement du contenu enregistré
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave macro)
- MCIWndSaveDialog macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673165"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="6828b-105">Enregistrement du contenu enregistré</span><span class="sxs-lookup"><span data-stu-id="6828b-105">Saving Recorded Content</span></span>

<span data-ttu-id="6828b-106">Une fois l’enregistrement terminé, vous pouvez enregistrer le contenu à l’aide de la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) ou [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) , ou en utilisant la fonction [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) avec **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="6828b-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="6828b-107">La macro **MCIWndSave** enregistre les données dans le fichier associé à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6828b-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="6828b-108">La macro **MCIWndSaveDialog** permet à l’utilisateur de spécifier un nom de fichier et d’enregistrer les données enregistrées dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6828b-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="6828b-109">La fonction **GetSaveFileNamePreview** affiche la boîte de dialogue **Enregistrer** sous pour choisir un fichier et permet à l’utilisateur d’afficher un aperçu (lecture) du fichier.</span><span class="sxs-lookup"><span data-stu-id="6828b-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="6828b-110">Lorsque le nom d’un fichier existant est spécifié dans la boîte de dialogue **Enregistrer** sous, **GetSaveFileNamePreview** fournit un petit contrôle dans la boîte de dialogue pour permettre à l’utilisateur d’afficher un aperçu du contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="6828b-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="6828b-111">Vous pouvez enregistrer les données enregistrées dans un fichier sélectionné avec **GetSaveFileNamePreview** à l’aide de **MCIWndSave**.</span><span class="sxs-lookup"><span data-stu-id="6828b-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 





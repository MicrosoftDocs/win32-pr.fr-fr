---
title: Enregistrement des données capturées dans un nouveau fichier
description: Enregistrement des données capturées dans un nouveau fichier
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Message WM_CAP_FILE_SAVEAS
- capFileSaveAs macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673166"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="c8806-105">Enregistrement des données capturées dans un nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="c8806-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="c8806-106">Si l’utilisateur souhaite enregistrer les données capturées, l’application doit enregistrer le contenu du fichier de capture dans un autre fichier à l’aide du message de [**fichier d' \_ \_ \_ enregistrement de l’embout WM**](wm-cap-file-saveas.md) (ou de la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ).</span><span class="sxs-lookup"><span data-stu-id="c8806-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="c8806-107">Ce message ne modifie pas le nom ou le contenu du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="c8806-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="c8806-108">Votre application doit spécifier un nom pour le nouveau fichier, car le fichier de capture conserve son nom de fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="c8806-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="c8806-109">En règle générale, un fichier de capture est préalloué pour le plus grand segment de capture prévu, et seule une partie de celui-ci peut être utilisée pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="c8806-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="c8806-110">Ce message copie uniquement la partie du fichier de capture contenant les données de capture.</span><span class="sxs-lookup"><span data-stu-id="c8806-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 





---
description: Je dispose d’un fichier AVI contenant un flux de Windows Media Video.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: Je dispose d’un fichier AVI contenant un flux de Windows Media Video. Comment puis-je le convertir en fichier WMV ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538250"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="bc136-104">Je dispose d’un fichier AVI contenant un flux de Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="bc136-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="bc136-105">Comment puis-je le convertir en fichier WMV ?</span><span class="sxs-lookup"><span data-stu-id="bc136-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="bc136-106">Les interfaces de codec vidéo et Windows Media Audio ne fournissent pas de méthodes pour créer des fichiers à l’aide du format ASF (Advanced Systems Format), qui est le format utilisé pour les fichiers WMV.</span><span class="sxs-lookup"><span data-stu-id="bc136-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="bc136-107">Si vous souhaitez convertir un fichier (à l’aide d’un conteneur) en fichier ASF, vous devez utiliser les objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bc136-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="bc136-108">Récupérez les exemples de média Windows compressés à partir du fichier source et transmettez-les à l’objet writer en tant qu’exemples de flux.</span><span class="sxs-lookup"><span data-stu-id="bc136-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="bc136-109">Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Windows Media Format 9 Series.</span><span class="sxs-lookup"><span data-stu-id="bc136-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc136-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc136-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc136-111">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="bc136-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 




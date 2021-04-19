---
description: Comment faire décompresser des flux à partir d’un fichier AVI ou d’un autre fichier sur lequel je n’ai pas d’informations de format ?
ms.assetid: 980f52f4-17a4-4871-9269-f9e0b97416c6
title: Comment faire décompresser des flux à partir d’un fichier AVI ou d’un autre fichier sur lequel je n’ai pas d’informations de format ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad230c36097a93b3d2d41ddffb35600d0616ea5f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525790"
---
# <a name="how-do-i-decompress-streams-from-an-avi-file-or-other-file-about-which-i-have-no-format-information"></a><span data-ttu-id="22e1e-103">Comment faire décompresser des flux à partir d’un fichier AVI ou d’un autre fichier sur lequel je n’ai pas d’informations de format ?</span><span class="sxs-lookup"><span data-stu-id="22e1e-103">How do I decompress streams from an AVI file or other file about which I have no format information?</span></span>

<span data-ttu-id="22e1e-104">Sans les informations de mise en forme, y compris les données de format étendu, vous ne pouvez pas décompresser les données qui ont été encodées avec un codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22e1e-104">Without format information, including extended format data, you cannot decompress data that was encoded with a Windows Media codec.</span></span> <span data-ttu-id="22e1e-105">Les codecs ont été conçus pour créer des flux de données à utiliser avec le conteneur de fichiers ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="22e1e-105">The codecs were designed to create data streams for use with the Advanced Systems Format (ASF) file container.</span></span> <span data-ttu-id="22e1e-106">La section d’en-tête d’un fichier ASF stocke les informations de mise en forme pour tous les flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="22e1e-106">The header section of an ASF file stores the format information for all of the streams in the file.</span></span> <span data-ttu-id="22e1e-107">Lorsque vous utilisez le contenu encodé à l’aide de l’un des codecs Windows Media Audio et vidéo en dehors d’un fichier ASF, vous devez vous assurer que les informations de format sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="22e1e-107">When you use content encoded using one of the Windows Media Audio and Video codecs outside of an ASF file, you must ensure that the format information is available.</span></span> <span data-ttu-id="22e1e-108">La façon de procéder varie d’un conteneur à un autre.</span><span class="sxs-lookup"><span data-stu-id="22e1e-108">The way to do this varies from one container to another.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e1e-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22e1e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e1e-110">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="22e1e-110">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 




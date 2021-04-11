---
title: Lire à partir d’un fichier
description: Lire à partir d’un fichier
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029627"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="5bf1e-104">Lire à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="5bf1e-104">Reading from a File</span></span>

<span data-ttu-id="5bf1e-105">Vous pouvez récupérer des informations sur un fichier ouvert à l’aide de la fonction [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) .</span><span class="sxs-lookup"><span data-stu-id="5bf1e-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="5bf1e-106">Cette fonction remplit la structure [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) avec des informations telles que le débit de données maximal, le nombre de flux dans le fichier, si le fichier utilise un index et si le fichier est protégé par des droits d’auteur.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="5bf1e-107">Pour récupérer des informations supplémentaires dans un fichier AVI, utilisez la fonction [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) .</span><span class="sxs-lookup"><span data-stu-id="5bf1e-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="5bf1e-108">Des informations supplémentaires sont applicables à l’ensemble du fichier et ne sont pas incluses dans les en-têtes de fichier normaux.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="5bf1e-109">Par exemple, le nom de la société ou de la personne qui détient les droits d’auteur d’un fichier peut être des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="5bf1e-110">Les informations supplémentaires ne sont pas conformes à un format spécifique. Il peut s’agir d’un fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="5bf1e-111">**AVIFileReadData** retourne les informations supplémentaires dans une mémoire tampon fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5bf1e-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 





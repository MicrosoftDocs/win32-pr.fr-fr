---
description: Le spouleur d’impression surveille les travaux d’impression en cours et l’imprimante cible pour déterminer le moment approprié pour l’impression d’un travail.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Processeur d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519885"
---
# <a name="print-processor"></a><span data-ttu-id="a12a1-103">Processeur d’impression</span><span class="sxs-lookup"><span data-stu-id="a12a1-103">Print Processor</span></span>

<span data-ttu-id="a12a1-104">Le spouleur d’impression surveille les travaux d’impression en cours et l’imprimante cible pour déterminer le moment approprié pour l’impression d’un travail.</span><span class="sxs-lookup"><span data-stu-id="a12a1-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="a12a1-105">Une fois que le spouleur a déterminé qu’un travail doit être imprimé, il appelle le processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="a12a1-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="a12a1-106">Le processeur d’impression est un plug-in qui traite les données du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="a12a1-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="a12a1-107">Utilisez les fonctions suivantes pour travailler avec des processeurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="a12a1-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="a12a1-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="a12a1-108">Function</span></span>                                                           | <span data-ttu-id="a12a1-109">Description</span><span class="sxs-lookup"><span data-stu-id="a12a1-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a12a1-110">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="a12a1-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="a12a1-111">Installe un processeur d’impression sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a12a1-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="a12a1-112">**DeletePrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="a12a1-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="a12a1-113">Supprime un processeur d’imprimante d’un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a12a1-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="a12a1-114">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="a12a1-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="a12a1-115">Énumère les types de données pris en charge par un processeur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="a12a1-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="a12a1-116">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="a12a1-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="a12a1-117">Énumère les processeurs d’impression installés sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a12a1-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="a12a1-118">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="a12a1-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="a12a1-119">Récupère le chemin d’accès du processeur d’impression sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a12a1-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 




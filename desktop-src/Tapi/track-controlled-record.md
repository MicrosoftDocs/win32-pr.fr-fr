---
description: Cette rubrique fournit une procédure pour effectuer l’enregistrement contrôlé par suivi des flux audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Enregistrement Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865689"
---
# <a name="track-controlled-record"></a><span data-ttu-id="535f4-103">Enregistrement Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="535f4-103">Track-Controlled Record</span></span>

<span data-ttu-id="535f4-104">Cette rubrique fournit une procédure pour effectuer l’enregistrement contrôlé par suivi des flux audio.</span><span class="sxs-lookup"><span data-stu-id="535f4-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="535f4-105">**Pour effectuer un enregistrement contrôlé des flux audio**</span><span class="sxs-lookup"><span data-stu-id="535f4-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="535f4-106">Sélectionnez fichier suivre les terminaux dans les flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="535f4-107">Créez le terminal d’enregistrement de fichier.</span><span class="sxs-lookup"><span data-stu-id="535f4-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="535f4-108">Définissez le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="535f4-108">Set the file name.</span></span>
4.  <span data-ttu-id="535f4-109">Énumérer les flux sur l’appel TAPI.</span><span class="sxs-lookup"><span data-stu-id="535f4-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="535f4-110">Pour ces étapes, consultez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="535f4-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="535f4-111">Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal d’enregistrement de fichier pour démarrer l’enregistrement de flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="535f4-112">**Pour énumérer des flux sur l’appel TAPI**</span><span class="sxs-lookup"><span data-stu-id="535f4-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="535f4-113">Créer une piste du même type et de la même direction audio que le flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="535f4-114">Définissez les propriétés de suivi pour le format audio.</span><span class="sxs-lookup"><span data-stu-id="535f4-114">Set the track properties for audio format.</span></span> <span data-ttu-id="535f4-115">Si la valeur n’est pas définie, le format sera le même que celui du flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="535f4-116">Sélectionnez la piste dans le flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-116">Select the track on the stream.</span></span>

<span data-ttu-id="535f4-117">Si une piste est sélectionnée sur plusieurs flux, cela implique la combinaison de flux.</span><span class="sxs-lookup"><span data-stu-id="535f4-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 




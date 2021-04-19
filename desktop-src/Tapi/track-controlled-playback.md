---
description: Les étapes suivantes sont effectuées pour la lecture contrôlée par suivi.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Lecture Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545826"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="7981a-103">Lecture Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="7981a-103">Track-Controlled Playback</span></span>

<span data-ttu-id="7981a-104">Pour effectuer une lecture contrôlée par suivi, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7981a-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="7981a-105">Sélectionnez le suivi des terminaux sur les flux.</span><span class="sxs-lookup"><span data-stu-id="7981a-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="7981a-106">Créez le terminal de lecture de fichier.</span><span class="sxs-lookup"><span data-stu-id="7981a-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="7981a-107">Définir les propriétés : le nom et le type de stockage du fichier.</span><span class="sxs-lookup"><span data-stu-id="7981a-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="7981a-108">À l’aide d’une méthode sur le terminal de lecture de fichier, énumérez les terminaux de suivi de fichier.</span><span class="sxs-lookup"><span data-stu-id="7981a-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="7981a-109">Énumérer les flux sur l’appel TAPI.</span><span class="sxs-lookup"><span data-stu-id="7981a-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="7981a-110">Sélectionnez le terminal file Track dans le flux.</span><span class="sxs-lookup"><span data-stu-id="7981a-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="7981a-111">Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal de lecture de fichier pour démarrer la lecture des données enregistrées dans les flux TAPI.</span><span class="sxs-lookup"><span data-stu-id="7981a-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 




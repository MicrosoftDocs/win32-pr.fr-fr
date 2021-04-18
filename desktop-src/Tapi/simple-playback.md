---
description: La rubrique suivante explique comment effectuer une lecture simple.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Lecture simple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523042"
---
# <a name="simple-playback"></a><span data-ttu-id="cc725-103">Lecture simple</span><span class="sxs-lookup"><span data-stu-id="cc725-103">Simple Playback</span></span>

<span data-ttu-id="cc725-104">La rubrique suivante explique comment effectuer une lecture simple.</span><span class="sxs-lookup"><span data-stu-id="cc725-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="cc725-105">**Pour effectuer une lecture simple**</span><span class="sxs-lookup"><span data-stu-id="cc725-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="cc725-106">Sélectionnez le terminal de lecture de fichier au niveau de l’appel.</span><span class="sxs-lookup"><span data-stu-id="cc725-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="cc725-107">Créez le terminal de lecture sur l’appel TAPI.</span><span class="sxs-lookup"><span data-stu-id="cc725-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="cc725-108">Définir les propriétés : le nom et le type de stockage du fichier.</span><span class="sxs-lookup"><span data-stu-id="cc725-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="cc725-109">Appelez la méthode [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sur le terminal de lecture de fichier pour démarrer la lecture des flux.</span><span class="sxs-lookup"><span data-stu-id="cc725-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="cc725-110">L’exemple de code suivant illustre une lecture simple.</span><span class="sxs-lookup"><span data-stu-id="cc725-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="cc725-111">Tout d’abord, utilisez l’interface [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) pour créer le terminal pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cc725-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="cc725-112">Cela indique au TSP/MSP d’effectuer la lecture des fichiers sur cet appel.</span><span class="sxs-lookup"><span data-stu-id="cc725-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="cc725-113">Le TSP/MSP crée un terminal pour l’application à utiliser et le retourne en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="cc725-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="cc725-114">Récupérez le pointeur d’interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) à partir de l’interface terminal et utilisez-le pour définir le nom de fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="cc725-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="cc725-115">En supposant que le fichier contienne un flux audio, et que l’appel possède un flux audio de capture, le contenu audio du fichier est lu sur ce flux.</span><span class="sxs-lookup"><span data-stu-id="cc725-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 




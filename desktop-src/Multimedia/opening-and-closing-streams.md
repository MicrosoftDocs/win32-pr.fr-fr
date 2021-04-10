---
title: Ouverture et fermeture de flux
description: Ouverture et fermeture de flux
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream fonction)
- AVIStreamRelease fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028926"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="d614c-105">Ouverture et fermeture de flux</span><span class="sxs-lookup"><span data-stu-id="d614c-105">Opening and Closing Streams</span></span>

<span data-ttu-id="d614c-106">L’ouverture de flux de données est semblable à l’ouverture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d614c-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="d614c-107">Vous pouvez ouvrir un flux à l’aide de la fonction [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) .</span><span class="sxs-lookup"><span data-stu-id="d614c-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="d614c-108">Cette fonction crée une interface de flux, place un handle du flux dans l’interface et retourne un pointeur vers l’interface.</span><span class="sxs-lookup"><span data-stu-id="d614c-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="d614c-109">**AVIFileGetStream** gère également un décompte de références des applications qui ont ouvert un flux, mais pas celles qui l’ont fermé.</span><span class="sxs-lookup"><span data-stu-id="d614c-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="d614c-110">Si vous souhaitez accéder à un flux unique dans un fichier, vous pouvez ouvrir le fichier et le flux à l’aide de la fonction [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) .</span><span class="sxs-lookup"><span data-stu-id="d614c-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="d614c-111">Cette fonction combine les arguments Operations et Function des fonctions [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) et **AVIFileGetStream** .</span><span class="sxs-lookup"><span data-stu-id="d614c-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="d614c-112">Pour accéder à plusieurs flux dans un fichier, utilisez **AVIFileOpen** une fois suivi de plusieurs appels à **AVIFileGetStream**.</span><span class="sxs-lookup"><span data-stu-id="d614c-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="d614c-113">Vous pouvez incrémenter le décompte de références d’un flux à l’aide de la fonction [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) pour garder un flux ouvert lors de l’utilisation d’une fonction qui fermerait normalement le flux.</span><span class="sxs-lookup"><span data-stu-id="d614c-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="d614c-114">Vous pouvez fermer un flux à l’aide de la fonction [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="d614c-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="d614c-115">Cette fonction décrémente le décompte de références du flux et la ferme lorsque le nombre de références atteint zéro.</span><span class="sxs-lookup"><span data-stu-id="d614c-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="d614c-116">Vos applications doivent équilibrer le nombre de références en incluant un appel à **AVIStreamRelease** pour chaque utilisation de la fonction [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** ou **AVIStreamOpenFromFile** .</span><span class="sxs-lookup"><span data-stu-id="d614c-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="d614c-117">Lorsque vous publiez un flux qui a été ouvert à l’aide de **AVIStreamOpenFromFile**, avifile ferme le fichier contenant le flux.</span><span class="sxs-lookup"><span data-stu-id="d614c-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="d614c-118">Si votre application libère un fichier qui a des flux de données ouverts, AVIFile ne ferme pas les flux tant que tous les flux n’ont pas été libérés.</span><span class="sxs-lookup"><span data-stu-id="d614c-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 





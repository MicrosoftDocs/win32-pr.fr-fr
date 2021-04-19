---
title: Ouverture et fermeture de fichiers
description: Ouverture et fermeture de fichiers
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen fonction)
- AVIFileRelease fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535121"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="2407d-105">Ouverture et fermeture de fichiers</span><span class="sxs-lookup"><span data-stu-id="2407d-105">Opening and Closing Files</span></span>

<span data-ttu-id="2407d-106">Une application doit ouvrir un fichier AVI avant la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="2407d-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="2407d-107">Pour ouvrir un fichier AVI, utilisez la fonction [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="2407d-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="2407d-108">**AVIFileOpen** retourne l’adresse d’une interface de fichier AVI qui contient le handle du fichier ouvert et incrémente le décompte de références du fichier.</span><span class="sxs-lookup"><span data-stu-id="2407d-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="2407d-109">La fonction **AVIFileOpen** prend en charge le d’indicateurs utilisés avec la fonction [OpenFile](/documentation/) .</span><span class="sxs-lookup"><span data-stu-id="2407d-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="2407d-110">Si une application écrit dans un fichier existant, elle doit inclure l' \_ indicateur d’écriture dans **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="2407d-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="2407d-111">De même, si votre application crée et écrit dans un nouveau fichier, vous devez inclure le de \_ Create et des \_ indicateurs d’écriture dans **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="2407d-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="2407d-112">Lorsque vous ouvrez un fichier à l’aide de **AVIFileOpen**, vous pouvez utiliser un gestionnaire de fichiers par défaut ou vous pouvez spécifier un gestionnaire de fichiers personnalisé pour lire et écrire dans le fichier et ses flux de données.</span><span class="sxs-lookup"><span data-stu-id="2407d-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="2407d-113">Dans les deux cas, AVIFile recherche le gestionnaire de fichiers correct à utiliser dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2407d-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="2407d-114">Vous devez vous assurer que les gestionnaires de fichiers personnalisés se trouvent dans le registre avant qu’une application puisse y accéder.</span><span class="sxs-lookup"><span data-stu-id="2407d-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="2407d-115">Vous pouvez incrémenter le décompte de références d’un fichier à l’aide de la fonction [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) .</span><span class="sxs-lookup"><span data-stu-id="2407d-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="2407d-116">Par exemple, vous souhaiterez peut-être effectuer cette opération lors du passage d’un handle de l’interface de fichier à une autre application, ou lorsque vous souhaitez conserver un fichier ouvert lors de l’utilisation d’une fonction qui fermerait normalement le fichier.</span><span class="sxs-lookup"><span data-stu-id="2407d-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="2407d-117">Vous pouvez fermer un fichier à l’aide de la fonction [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="2407d-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="2407d-118">La fonction **AVIFileRelease** décrémente le décompte de références d’un fichier AVI, enregistre les modifications apportées au fichier et, lorsque le nombre de références atteint zéro, ferme le fichier.</span><span class="sxs-lookup"><span data-stu-id="2407d-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="2407d-119">Vos applications doivent équilibrer le nombre de références en incluant un appel à **AVIFileRelease** pour chaque utilisation de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) et **AVIFileAddRef**.</span><span class="sxs-lookup"><span data-stu-id="2407d-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="2407d-120">Une application peut ouvrir un fichier avec un ou plusieurs threads de programme.</span><span class="sxs-lookup"><span data-stu-id="2407d-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="2407d-121">Toutefois, pour des performances optimales, un seul thread doit accéder au fichier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="2407d-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 
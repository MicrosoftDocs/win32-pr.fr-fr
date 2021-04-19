---
title: Accélération GPU dans WSL
description: Direct Machine Learning (DirectML) alimente le GPU-accelleration dans le sous-système Windows pour Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544158"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="9654b-103">Formation ML accélérée par GPU</span><span class="sxs-lookup"><span data-stu-id="9654b-103">GPU accelerated ML training</span></span>

![Illustration Windows ML](images/winml-graphic.png)

<span data-ttu-id="9654b-105">Cette documentation couvre ce qui est actuellement pris en charge par la préversion de formation du GPU accélérée Machine Learning (ML) pour le [sous-système Windows pour Linux](/windows/wsl/about) (WSL) et native Windows.</span><span class="sxs-lookup"><span data-stu-id="9654b-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="9654b-106">Cette version préliminaire prend en charge les scénarios professionnels et débutants.</span><span class="sxs-lookup"><span data-stu-id="9654b-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="9654b-107">Vous trouverez ci-dessous des pointeurs vers des guides pas à pas sur la façon d’obtenir la configuration de votre système en fonction de votre niveau d’expertise dans ML, le fournisseur de GPU et la bibliothèque de logiciels que vous avez l’intention d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9654b-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="9654b-108">Les fonctionnalités suivantes sont en version préliminaire et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="9654b-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="9654b-109">Professionnel</span><span class="sxs-lookup"><span data-stu-id="9654b-109">Professionals</span></span>

<span data-ttu-id="9654b-110">Si vous êtes un spécialiste des données professionnels qui utilise un environnement Linux natif au quotidien pour le développement et l’expérimentation de la boucle interne, et que vous disposez d’un GPU NVIDIA, nous vous recommandons de configurer la version [préliminaire de NVIDIA CUDA dans WSL 2.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="9654b-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="9654b-111">Élèves et débutants</span><span class="sxs-lookup"><span data-stu-id="9654b-111">Students and beginners</span></span> 

<span data-ttu-id="9654b-112">Si vous êtes étudiant ou débutant et que vous souhaitez commencer à développer vos connaissances dans l’espace ML, nous vous recommandons de configurer le TensorFlow avec le package backend DirectML.</span><span class="sxs-lookup"><span data-stu-id="9654b-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="9654b-113">Ce package accélère actuellement les workflows sur les processeurs graphiques AMD et Intel.</span><span class="sxs-lookup"><span data-stu-id="9654b-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="9654b-114">La prise en charge des GPU NVIDIA sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="9654b-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="9654b-115">Pour ceux qui sont plus familiers avec un environnement Linux natif qui prend en main les workflows ML, nous vous recommandons d’exécuter le [package TensorFlow avec DirectML à l’intérieur de WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="9654b-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="9654b-116">Pour ceux qui sont plus familiers avec les fenêtres qui sont en cours de prise en main des flux de travail ML, nous vous recommandons de configurer le [package TensorFlow avec DirectML sur des fenêtres natives](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="9654b-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="9654b-117">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9654b-117">Next steps</span></span>

* <span data-ttu-id="9654b-118">[Activez la version préliminaire de NVIDIA CUDA dans WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="9654b-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="9654b-119">[Activez TensorFlow avec le package DirectML dans WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="9654b-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="9654b-120">[Activez TensorFlow avec le package DirectML sur Windows natif](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="9654b-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>
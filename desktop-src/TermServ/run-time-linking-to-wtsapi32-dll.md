---
title: Run-Time la liaison à Wtsapi32.dll
description: Votre application peut utiliser l’API Services Bureau à distance pour établir une liaison dynamique avec l' Wtsapi32.dll au moment de l’exécution. Pour ce faire, votre application doit appeler la fonction LoadLibrary pour charger Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382349"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="8645e-104">Run-Time la liaison à Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="8645e-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="8645e-105">Si votre application s’exécute dans un environnement qui n’est pas un environnement Services Bureau à distance, mais que vous souhaitez que votre application fournisse des fonctionnalités supplémentaires lorsqu’elle s’exécute dans un environnement Services Bureau à distance, l’application peut utiliser l’API Services Bureau à distance pour implémenter les fonctionnalités supplémentaires et établir une liaison dynamique avec les Wtsapi32.dll au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="8645e-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="8645e-106">Pour ce faire, votre application doit appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8645e-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="8645e-107">Si l’appel de **LoadLibrary** échoue, votre application peut s’exécuter à l’aide de ses fonctionnalités de base.</span><span class="sxs-lookup"><span data-stu-id="8645e-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="8645e-108">Si **LoadLibrary** s’exécute correctement, votre application peut appeler la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer les pointeurs vers les fonctions services Bureau à distance que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="8645e-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="8645e-109">Si votre application est conçue uniquement pour un environnement Services Bureau à distance, la liaison dynamique n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8645e-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="8645e-110">Dans ce cas, vous pouvez inclure Wtsapi32. h et établir un lien avec Wtsapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="8645e-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="8645e-111">Ensuite, si votre application démarre dans un environnement autre que Services Bureau à distance, elle se termine car Wtsapi32.dll n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="8645e-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="8645e-112">Pour plus d’informations sur la façon de déterminer si votre application s’exécute dans un environnement Services Bureau à distance, consultez [détection de l’environnement services Bureau à distance](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8645e-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8645e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8645e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8645e-114">Instructions de programmation générales</span><span class="sxs-lookup"><span data-stu-id="8645e-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 
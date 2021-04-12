---
description: Essayez-vous de trouver plus d’informations sur les objets Direct3D pendant le débogage ? Par exemple, la capture d’écran suivante montre ce que vous voyez généralement lorsque vous examinez une interface Direct3D dans la fenêtre Espion.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Activation des informations de débogage Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108403"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="fb421-104">Activation des informations de débogage Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fb421-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="fb421-105">Essayez-vous de trouver plus d’informations sur les objets Direct3D pendant le débogage ?</span><span class="sxs-lookup"><span data-stu-id="fb421-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="fb421-106">Par exemple, la capture d’écran suivante montre ce que vous voyez généralement lorsque vous examinez une interface Direct3D dans la fenêtre Espion.</span><span class="sxs-lookup"><span data-stu-id="fb421-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![capture d’écran d’une interface Direct3D dans la fenêtre Espion](images/d3d-debug-info1.png)

<span data-ttu-id="fb421-108">Vous pouvez activer les objets de débogage de base afin qu’un objet mis en miroir qui contient toutes les propriétés de l’objet puisse être affiché dans la fenêtre Espion.</span><span class="sxs-lookup"><span data-stu-id="fb421-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="fb421-109">Incluez simplement la \# définition suivante dans votre code avant le fichier d3d9. h :</span><span class="sxs-lookup"><span data-stu-id="fb421-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="fb421-110">Pour activer les informations de débogage, la \# définition doit être générée avant le fichier d3d9. h (tout programme qui utilise DXUT active automatiquement les \_ informations de débogage D3D \_ lorsque le programme est compilé pour le débogage).</span><span class="sxs-lookup"><span data-stu-id="fb421-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="fb421-111">Si vous exécutez un exemple du kit de développement logiciel (SDK), vous pouvez le voir dans DXStdAfx. h (ce qui affecte tous les exemples C++).</span><span class="sxs-lookup"><span data-stu-id="fb421-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="fb421-112">Vous devez également exécuter le runtime Direct3D de débogage (qui peut être activé à partir du panneau de configuration, si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="fb421-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="fb421-113">Voici un exemple d’utilisation de l' [exemple BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="fb421-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="fb421-114">Ajoutez la \# définition au fichier Dxstdafx. h avant la ligne 37.</span><span class="sxs-lookup"><span data-stu-id="fb421-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="fb421-115">Générez un projet de débogage.</span><span class="sxs-lookup"><span data-stu-id="fb421-115">Build a debug project.</span></span>
3.  <span data-ttu-id="fb421-116">Définir un point d’arrêt à la ligne 307 dans BasicHLSL. cpp</span><span class="sxs-lookup"><span data-stu-id="fb421-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="fb421-117">Exécutez le débogueur.</span><span class="sxs-lookup"><span data-stu-id="fb421-117">Run the debugger.</span></span>

<span data-ttu-id="fb421-118">La capture d’écran suivante montre le type d’informations détaillées que vous pouvez obtenir à propos d’un objet de texture Direct3D dans la fenêtre Espion.</span><span class="sxs-lookup"><span data-stu-id="fb421-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![capture d’écran d’un objet de texture Direct3D dans la fenêtre Espion](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="fb421-120">Les noms des propriétés de l’objet sont visibles et les valeurs sont correctes uniquement lorsque le runtime de débogage est activé.</span><span class="sxs-lookup"><span data-stu-id="fb421-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="fb421-121">En cas d’exécution sur le runtime de vente au détail, les valeurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="fb421-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="fb421-122">Utiliser la pile des appels pour le débogage étendu</span><span class="sxs-lookup"><span data-stu-id="fb421-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="fb421-123">Lorsque le débogage Direct3D est activé, vous pouvez également examiner une pile des appels chaque fois qu’un objet est créé.</span><span class="sxs-lookup"><span data-stu-id="fb421-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="fb421-124">Cela rend votre application très lente, mais peut être utilisée pour vérifier les fuites de ressources.</span><span class="sxs-lookup"><span data-stu-id="fb421-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="fb421-125">Pour écrire la pile des appels, affectez la valeur 1 à la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="fb421-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="fb421-126">La génération de votre application avec le débogage activé vous donne accès à cette variable supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="fb421-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="fb421-127">Cette variable stockera la pile des appels chaque fois qu’un objet sera créé.</span><span class="sxs-lookup"><span data-stu-id="fb421-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="fb421-128">Cela rend votre application très lente, mais peut être utilisée pour déboguer les fuites de ressources.</span><span class="sxs-lookup"><span data-stu-id="fb421-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb421-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb421-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb421-130">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="fb421-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 




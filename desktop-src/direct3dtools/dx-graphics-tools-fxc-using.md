---
title: Compilation hors connexion
description: L’outil Effect-compiler Tool (fxc.exe) est conçu pour la compilation hors connexion des nuanceurs HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, compilation hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729909"
---
# <a name="offline-compiling"></a><span data-ttu-id="d584e-104">Compilation hors connexion</span><span class="sxs-lookup"><span data-stu-id="d584e-104">Offline compiling</span></span>

<span data-ttu-id="d584e-105">L’outil Effect-compiler Tool (fxc.exe) est conçu pour la compilation hors connexion des nuanceurs HLSL.</span><span class="sxs-lookup"><span data-stu-id="d584e-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="d584e-106">Compilation avec le compilateur actuel</span><span class="sxs-lookup"><span data-stu-id="d584e-106">Compiling with the current compiler</span></span>

<span data-ttu-id="d584e-107">Les modèles de nuanceur pris en charge par le compilateur actuel sont affichés dans [profils](dx-graphics-tools-fxc-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d584e-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="d584e-108">Cet exemple compile un nuanceur de pixels pour la cible du modèle de nuanceur 5,1.</span><span class="sxs-lookup"><span data-stu-id="d584e-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="d584e-109">Dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="d584e-109">In this example:</span></span>

-   <span data-ttu-id="d584e-110">PS \_ 5 \_ 1 est le profil cible.</span><span class="sxs-lookup"><span data-stu-id="d584e-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="d584e-111">PixelShader1. fxc est le fichier objet de sortie contenant le nuanceur compilé.</span><span class="sxs-lookup"><span data-stu-id="d584e-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="d584e-112">PixelShader1. HLSL est la source.</span><span class="sxs-lookup"><span data-stu-id="d584e-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="d584e-113">Les options de débogage incluent des options supplémentaires pour désactiver les optimisations du compilateur (OD) et activer les informations de débogage (ZI) comme les numéros de ligne et les symboles.</span><span class="sxs-lookup"><span data-stu-id="d584e-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="d584e-114">Pour obtenir la liste complète des options de ligne de commande, consultez la page [syntaxe](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="d584e-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="d584e-115">Compilation avec le compilateur hérité</span><span class="sxs-lookup"><span data-stu-id="d584e-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="d584e-116">À partir de Direct3D 10, certains modèles de nuanceur ne sont plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d584e-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="d584e-117">Celles-ci incluent les modèles de nuanceur de pixels : PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 et PS \_ 1 \_ 4 qui prennent en charge des ressources très limitées et qui dépendent du matériel.</span><span class="sxs-lookup"><span data-stu-id="d584e-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="d584e-118">Le compilateur a été repensé avec le modèle de nuanceur 2 (ou supérieur), ce qui permet d’améliorer l’efficacité de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d584e-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="d584e-119">Cela implique que vous soyez en cours d’exécution sur du matériel qui prend en charge les modèles de nuanceur 2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d584e-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="d584e-120">Notez également que vous devez consulter les notes de publication du kit de développement logiciel (SDK) associées à votre version du compilateur FXC pour le comportement affecté par le commutateur/GEC.</span><span class="sxs-lookup"><span data-stu-id="d584e-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="d584e-121">Utilisation de l’outil Effect-compiler dans un sous-processus</span><span class="sxs-lookup"><span data-stu-id="d584e-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="d584e-122">Si fxc.exe est généré en tant que sous-processus par une application, il est important de s’assurer que l’application recherche et lit les données dans les canaux de sortie ou d’erreur transmis à la fonction CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="d584e-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="d584e-123">Si l’application attend uniquement que le sous-processus se termine et que l’un des canaux soit plein, le sous-processus ne se terminera jamais.</span><span class="sxs-lookup"><span data-stu-id="d584e-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="d584e-124">L’exemple de code suivant illustre l’attente d’un sous-processus et la lecture des canaux de sortie et d’erreur attachés au sous-processus.</span><span class="sxs-lookup"><span data-stu-id="d584e-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="d584e-125">Le contenu du `WaitHandles` tableau correspond aux descripteurs du sous-processus, au canal pour stdout et au canal pour stderr.</span><span class="sxs-lookup"><span data-stu-id="d584e-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="d584e-126">Pour plus d’informations sur la génération d’un processus, consultez la page de référence pour [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="d584e-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d584e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d584e-127">Related topics</span></span>

* [<span data-ttu-id="d584e-128">Effect-Tool du compilateur</span><span class="sxs-lookup"><span data-stu-id="d584e-128">Effect-Compiler Tool</span></span>](fxc.md)
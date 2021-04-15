---
description: Chargement d’un graphique à partir d’un processus externe
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Chargement d’un graphique à partir d’un processus externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550063"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="c2ed1-103">Chargement d’un graphique à partir d’un processus externe</span><span class="sxs-lookup"><span data-stu-id="c2ed1-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="c2ed1-104">GraphEdit peut charger un graphique de filtre créé par un processus externe.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="c2ed1-105">Avec cette fonctionnalité, vous pouvez voir exactement quel graphique de filtre votre application génère, avec seulement une quantité minimale de code supplémentaire dans votre application.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="c2ed1-106">Cette fonctionnalité nécessite Windows 2000, Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="c2ed1-107">À compter de Windows Vista, vous devez inscrire proppage.dll pour activer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="c2ed1-108">Proppage.dll est inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="c2ed1-109">L’application doit inscrire l’instance du graphique de filtre dans la table ROT (Running Object Table).</span><span class="sxs-lookup"><span data-stu-id="c2ed1-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="c2ed1-110">Le ROT est une table de recherche accessible globalement qui effectue le suivi des objets en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="c2ed1-111">Les objets sont enregistrés dans le ROT par moniker.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="c2ed1-112">Pour vous connecter au graphique, GraphEdit recherche dans le ROT les monikers dont le nom d’affichage correspond à un format particulier :</span><span class="sxs-lookup"><span data-stu-id="c2ed1-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="c2ed1-113">où *X* est l’adresse hexadécimale du gestionnaire de graphique de filtre, et *Y* est l’ID de processus, également au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="c2ed1-114">Lorsque votre application crée d’abord le graphique de filtre, appelez la fonction suivante :</span><span class="sxs-lookup"><span data-stu-id="c2ed1-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="c2ed1-115">Cette fonction crée un moniker et une nouvelle entrée ROT pour le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="c2ed1-116">Le premier paramètre est un pointeur vers le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="c2ed1-117">Le deuxième paramètre reçoit une valeur qui identifie la nouvelle entrée ROT.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="c2ed1-118">Avant que l’application ne libère le graphique de filtre, appelez la fonction suivante pour supprimer l’entrée ROT.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="c2ed1-119">Le paramètre *pdwRegister* est l’identificateur retourné par la fonction AddToRot.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="c2ed1-120">L’exemple de code suivant montre comment appeler ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="c2ed1-121">Dans cet exemple, le code qui ajoute et supprime les entrées ROT est compilé de manière conditionnelle, afin qu’il ne soit inclus que dans les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="c2ed1-122">Pour afficher le graphique de filtre dans GraphEdit, exécutez votre application et GraphEdit en même temps.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="c2ed1-123">Dans le menu **fichier** GraphEdit, cliquez sur **se connecter au graphique distant...** Dans la boîte de dialogue **se connecter au graphique** , sélectionnez l’ID de processus (PID) de votre application, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="c2ed1-124">GraphEdit charge le graphique de filtre et l’affiche.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="c2ed1-125">N’utilisez pas d’autres fonctionnalités GraphEdit sur ce graphique ; cela peut entraîner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="c2ed1-126">Par exemple, n’ajoutez pas ou ne supprimez pas de filtres, ou arrêtez et démarrez le graphique.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="c2ed1-127">Fermez GraphEdit avant de quitter votre application.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="c2ed1-128">Votre application peut atteindre plusieurs assertions lorsqu’elle se termine.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="c2ed1-129">Vous pouvez les ignorer.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-129">You can ignore these.</span></span>

 

<span data-ttu-id="c2ed1-130">L’illustration suivante montre la boîte de dialogue **se connecter au graphique** .</span><span class="sxs-lookup"><span data-stu-id="c2ed1-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![se connecter au graphique](images/gedit-spy.png)

<span data-ttu-id="c2ed1-132">Quand GraphEdit charge le graphique, il s’exécute dans le contexte de l’application cible.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="c2ed1-133">Par conséquent, GraphEdit peut être bloqué, car il attend le thread.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="c2ed1-134">Par exemple, cela peut se produire si vous exécutez pas à pas votre code dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="c2ed1-135">Cette fonctionnalité doit être utilisée uniquement dans les versions Debug de votre application, et non dans les versions commerciales, car elle permet à d’autres applications d’afficher ou de contrôler le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="c2ed1-136">Connexion à un graphique distant à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="c2ed1-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="c2ed1-137">GraphEdit prend en charge une option de ligne de commande pour charger automatiquement un graphique distant au démarrage.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="c2ed1-138">La syntaxe est :</span><span class="sxs-lookup"><span data-stu-id="c2ed1-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="c2ed1-139">où *moniker* est un moniker créé à l’aide de la fonction AddToRot, décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="c2ed1-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2ed1-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2ed1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ed1-141">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="c2ed1-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




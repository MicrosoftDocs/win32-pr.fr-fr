---
description: Étant donné que, dans de nombreux cas, vous pourrez déboguer uniquement une partie de vos fonctionnalités de composants dans l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic une fois qu’ils ont été compilés. Étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Débogage de composants Visual Basic compilés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110642"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="c420f-104">Débogage de composants Visual Basic compilés</span><span class="sxs-lookup"><span data-stu-id="c420f-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="c420f-105">Étant donné que, dans de nombreux cas, vous serez en mesure de déboguer uniquement une partie des fonctionnalités de votre composant au sein de l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic après qu’ils ont été compilés.</span><span class="sxs-lookup"><span data-stu-id="c420f-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="c420f-106">Étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c420f-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="c420f-107">**Pour déboguer un composant Visual Basic dans l’environnement Visual C++**</span><span class="sxs-lookup"><span data-stu-id="c420f-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="c420f-108">Dans Visual Basic 6,0, ouvrez le projet Visual Basic que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="c420f-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="c420f-109">Dans le menu **fichier** , cliquez sur **créer un YourProject.dll**.</span><span class="sxs-lookup"><span data-stu-id="c420f-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="c420f-110">Dans la boîte de dialogue **créer un projet** , cliquez sur **options**.</span><span class="sxs-lookup"><span data-stu-id="c420f-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="c420f-111">Dans la boîte de dialogue **Propriétés du projet** , sous l’onglet **compiler** , cliquez sur **compiler en code natif** et **aucune optimisation** , puis activez la case à cocher **créer des informations de débogage symboliques** .</span><span class="sxs-lookup"><span data-stu-id="c420f-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="c420f-112">Cliquez sur **OK**, puis de nouveau sur **OK** pour compiler votre projet.</span><span class="sxs-lookup"><span data-stu-id="c420f-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="c420f-113">Déplacez la DLL compilée vers l’emplacement où les applications COM+ sont normalement installées.</span><span class="sxs-lookup"><span data-stu-id="c420f-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="c420f-114">Si vous ne déplacez pas la DLL, vous pouvez recevoir un message d’erreur vous informant que les informations de débogage symboliques pour la DLL n’ont pas pu être localisées.</span><span class="sxs-lookup"><span data-stu-id="c420f-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="c420f-115">Si vous avez des difficultés à faire en sorte que le débogueur s’arrête à des points d’arrêt dans votre composant, vérifiez que la DLL se trouve dans le répertoire des packages standard, supprimez le composant de son package, puis ajoutez de nouveau le composant.</span><span class="sxs-lookup"><span data-stu-id="c420f-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="c420f-116">Démarrez Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c420f-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="c420f-117">Dans le menu **fichier** , cliquez sur **ouvrir l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="c420f-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="c420f-118">Dans la boîte de dialogue **ouvrir l’espace de travail** , définissez **fichiers de type** sur **tous les fichiers ( \* . \* )**, sélectionnez votre composant compilé, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="c420f-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="c420f-119">Dans le menu **fichier** , cliquez sur **ouvrir** (pas sur **ouvrir l’espace de travail**) et ouvrez le module de Visual Basic (. bas), le formulaire (. frm) ou la classe (. CLS) que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="c420f-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="c420f-120">Dans le menu **projet** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="c420f-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="c420f-121">Dans la boîte de dialogue **paramètres du projet** , sous l’onglet **Déboguer** , sélectionnez **général** dans la zone **catégorie** .</span><span class="sxs-lookup"><span data-stu-id="c420f-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="c420f-122">Dans la zone **exécutable pour la session de débogage** , entrez le chemin d’accès complet de Dllhost.exe, suivi d’un argument spécifiant l’ID de processus de l’application com+ contenant le composant.</span><span class="sxs-lookup"><span data-stu-id="c420f-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="c420f-123">L’ID de processus se trouve sous l’onglet **général** de la boîte de dialogue **Propriétés** de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="c420f-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="c420f-124">Voici un exemple : C : \\ winnt \\ system32 \\Dllhost.exe/ProcessId : { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="c420f-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="c420f-125">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c420f-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c420f-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c420f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c420f-127">Prise en charge du débogage des Visual Basic COM+ avec MTS</span><span class="sxs-lookup"><span data-stu-id="c420f-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="c420f-128">Débogage dans l’IDE Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c420f-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 




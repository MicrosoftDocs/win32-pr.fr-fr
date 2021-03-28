---
description: Cette rubrique explique comment déboguer des dll d’extension de Shell et d’espace de noms.
title: Débogage avec l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525378"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="afafb-103">Débogage avec l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="afafb-103">Debugging with the Shell</span></span>

<span data-ttu-id="afafb-104">Cette rubrique explique comment déboguer des dll d’extension de Shell et d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="afafb-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="afafb-105">Exécution de l’interpréteur de commandes sous un débogueur</span><span class="sxs-lookup"><span data-stu-id="afafb-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="afafb-106">Exécution et test des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="afafb-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="afafb-107">Déchargement de la DLL</span><span class="sxs-lookup"><span data-stu-id="afafb-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="afafb-108">Exécution de l’interpréteur de commandes sous un débogueur</span><span class="sxs-lookup"><span data-stu-id="afafb-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="afafb-109">Pour déboguer votre extension, vous devez exécuter le shell à partir du débogueur.</span><span class="sxs-lookup"><span data-stu-id="afafb-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="afafb-110">Suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="afafb-110">Follow these steps:</span></span>

1.  <span data-ttu-id="afafb-111">Chargez le projet de l’extension dans le débogueur, mais ne l’exécutez pas.</span><span class="sxs-lookup"><span data-stu-id="afafb-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="afafb-112">Arrêtez l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="afafb-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="afafb-113">Pour Windows Vista et versions ultérieures :</span><span class="sxs-lookup"><span data-stu-id="afafb-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="afafb-114">Affichez le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="afafb-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="afafb-115">Appuyez sur CTRL + MAJ et cliquez avec le bouton droit sur l’arrière-plan de la moitié droite du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="afafb-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="afafb-116">Dans le menu qui s’affiche, choisissez **quitter l’Explorateur**.</span><span class="sxs-lookup"><span data-stu-id="afafb-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="afafb-117">Pour Windows XP :</span><span class="sxs-lookup"><span data-stu-id="afafb-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="afafb-118">Dans le menu **Démarrer** , choisissez **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="afafb-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="afafb-119">Appuyez sur CTRL + ALT + MAJ, puis cliquez sur **non** dans la boîte de dialogue **arrêter Windows** .</span><span class="sxs-lookup"><span data-stu-id="afafb-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="afafb-120">L’interpréteur de commandes est maintenant arrêté, mais toutes les autres applications sont toujours en cours d’exécution, y compris le débogueur.</span><span class="sxs-lookup"><span data-stu-id="afafb-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="afafb-121">Définissez le débogueur pour exécuter la DLL d’extension avec Explorer.exe à partir du répertoire **Windows** .</span><span class="sxs-lookup"><span data-stu-id="afafb-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="afafb-122">Exécutez le projet à partir du débogueur.</span><span class="sxs-lookup"><span data-stu-id="afafb-122">Run the project from the debugger.</span></span> <span data-ttu-id="afafb-123">L’interpréteur de commandes est lancé comme d’habitude, mais le débogueur est attaché au processus de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="afafb-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="afafb-124">Exécution et test des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="afafb-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="afafb-125">Vous pouvez exécuter et tester vos extensions dans un processus d’Explorateur Windows distinct pour éviter d’arrêter et de redémarrer le bureau et la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="afafb-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="afafb-126">Votre bureau et votre barre des tâches peuvent toujours être utilisés pendant l’exécution et le test des extensions.</span><span class="sxs-lookup"><span data-stu-id="afafb-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="afafb-127">Pour activer cette fonctionnalité, ajoutez l' \_ entrée de Registre DWORD suivante au registre.</span><span class="sxs-lookup"><span data-stu-id="afafb-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="afafb-128">Pour que cette entrée prenne effet, vous devez vous déconnecter et vous reconnecter.</span><span class="sxs-lookup"><span data-stu-id="afafb-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="afafb-129">Ce paramètre entraîne la création des fenêtres de bureau et de la barre des tâches dans un processus de Explorer.exe et toutes les autres fenêtres Explorateur et dossier à ouvrir dans un processus de Explorer.exe différent.</span><span class="sxs-lookup"><span data-stu-id="afafb-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="afafb-130">En plus de rendre plus pratique l’exécution et le test de vos extensions, ce paramètre rend également le bureau plus robuste en ce qui concerne les extensions d’environnement.</span><span class="sxs-lookup"><span data-stu-id="afafb-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="afafb-131">De nombreuses extensions de ce type (extensions de menu contextuel, par exemple) sont chargées dans le processus de Explorer.exe non Desktop.</span><span class="sxs-lookup"><span data-stu-id="afafb-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="afafb-132">Si ce processus se termine, le bureau et la barre des tâches ne seront pas affectés, et la fenêtre de l’Explorateur ou du dossier suivant recréera le processus terminé.</span><span class="sxs-lookup"><span data-stu-id="afafb-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="afafb-133">Déchargement de la DLL</span><span class="sxs-lookup"><span data-stu-id="afafb-133">Unloading the DLL</span></span>

<span data-ttu-id="afafb-134">L’interpréteur de commandes décharge automatiquement toute DLL lorsque son nombre d’utilisations est égal à zéro, mais uniquement après que la DLL n’a pas été utilisée pendant une période donnée.</span><span class="sxs-lookup"><span data-stu-id="afafb-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="afafb-135">Cette période inactive peut être inutilement longue, en particulier lors du débogage d’une DLL d’extension de Shell.</span><span class="sxs-lookup"><span data-stu-id="afafb-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="afafb-136">Vous pouvez raccourcir la période inactive en ajoutant les informations suivantes au registre.</span><span class="sxs-lookup"><span data-stu-id="afafb-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 




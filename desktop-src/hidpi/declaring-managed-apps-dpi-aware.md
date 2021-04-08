---
title: Développement d’une application WPF DPI par moniteur
description: Remarque Cette page couvre le développement WPF hérité pour Windows 8.1. Si vous développez des applications WPF pour Windows 10, consultez la documentation la plus récente sur GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interface utilisateur Windows, applications compatibles DPI
- Interface utilisateur Windows, haute résolution
- Applications prenant en charge DPI
- haute résolution
- écriture d’applications Win32 compatibles DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101640"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="f1f47-110">Développement d’une application WPF DPI par moniteur</span><span class="sxs-lookup"><span data-stu-id="f1f47-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="f1f47-111">**API importantes**</span><span class="sxs-lookup"><span data-stu-id="f1f47-111">**Important APIs**</span></span>

-   [<span data-ttu-id="f1f47-112">**SetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="f1f47-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="f1f47-113">**GetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="f1f47-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="f1f47-114">**GetDpiForMonitor**</span><span class="sxs-lookup"><span data-stu-id="f1f47-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="f1f47-115">**Cette page traite du développement WPF hérité pour Windows 8.1.**</span><span class="sxs-lookup"><span data-stu-id="f1f47-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="f1f47-116">Si vous développez des applications WPF pour Windows 10, consultez la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentation la plus récente sur GitHub.</a></span><span class="sxs-lookup"><span data-stu-id="f1f47-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="f1f47-117">Windows 8.1 offre aux développeurs de nouvelles fonctionnalités pour créer des applications de bureau qui prennent en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="f1f47-118">Pour tirer parti de cette fonctionnalité, une application par analyse prenant en charge DPI doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1f47-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="f1f47-119">Modifiez les dimensions des fenêtres pour conserver une taille physique qui semble cohérente sur n’importe quel affichage</span><span class="sxs-lookup"><span data-stu-id="f1f47-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="f1f47-120">Restructurer et restituer à nouveau les graphiques pour la nouvelle taille de fenêtre</span><span class="sxs-lookup"><span data-stu-id="f1f47-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="f1f47-121">Sélectionner les polices mises à l’échelle correctement pour le niveau PPP</span><span class="sxs-lookup"><span data-stu-id="f1f47-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="f1f47-122">Sélectionner et charger des ressources bitmap adaptées au niveau PPP</span><span class="sxs-lookup"><span data-stu-id="f1f47-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="f1f47-123">Pour faciliter la création d’une application prenant en charge la résolution par moniteur, Windows 8.1 fournit les Win32APIs Microsoft suivants :</span><span class="sxs-lookup"><span data-stu-id="f1f47-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="f1f47-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (ou entrée de manifeste PPP) définit le processus sur un niveau de sensibilisation PPP spécifié, qui détermine ensuite la façon dont Windows met à l’échelle l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="f1f47-125">Cela remplace [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="f1f47-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="f1f47-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) retourne le niveau de sensibilisation PPP.</span><span class="sxs-lookup"><span data-stu-id="f1f47-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="f1f47-127">Cela remplace [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="f1f47-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="f1f47-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) retourne la valeur PPP d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="f1f47-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="f1f47-129">La notification de fenêtre [**WM \_ DPICHANGED**](wm-dpichanged.md) est envoyée aux applications prenant en charge la résolution par moniteur lorsque la position d’une fenêtre change de telle sorte que la plus grande partie de sa zone croise une analyse avec une valeur PPP différente de la résolution avant modification de la position ou lorsque l’utilisateur déplace le curseur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f1f47-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="f1f47-130">Pour créer une application qui se redimensionne et s’affiche à nouveau lorsqu’un utilisateur la déplace vers un autre affichage, utilisez cette notification.</span><span class="sxs-lookup"><span data-stu-id="f1f47-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="f1f47-131">Pour plus d’informations sur les différents niveaux de reconnaissance PPP pris en charge pour les applications de bureau dans Windows 8.1 consultez la rubrique sur l' [écriture d’applications DPI-Aware Desktop et Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="f1f47-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="f1f47-132">Mise à l’échelle DPI et WPF</span><span class="sxs-lookup"><span data-stu-id="f1f47-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="f1f47-133">Les applications Windows Presentation Foundation (WPF) utilisent par défaut la prise en charge DPI système.</span><span class="sxs-lookup"><span data-stu-id="f1f47-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="f1f47-134">Pour obtenir les définitions des différents niveaux de reconnaissance PPP, consultez la rubrique [écriture de DPI-Aware bureau et des applications Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="f1f47-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="f1f47-135">Le système graphique WPF utilise des unités indépendantes du périphérique pour permettre la résolution et l’indépendance des appareils.</span><span class="sxs-lookup"><span data-stu-id="f1f47-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="f1f47-136">WPF met automatiquement à l’échelle chaque pixel indépendant de l’appareil en fonction de la résolution système actuelle.</span><span class="sxs-lookup"><span data-stu-id="f1f47-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="f1f47-137">Cela permet aux applications WPF de se mettre à l’échelle automatiquement quand la valeur PPP du moniteur sur lequel se trouve la fenêtre correspond à la même résolution système.</span><span class="sxs-lookup"><span data-stu-id="f1f47-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="f1f47-138">Toutefois, étant donné que les applications WPF prennent en charge le système dpi, l’application est mise à l’échelle par le système d’exploitation lorsque l’application est déplacée vers un moniteur avec une résolution différente ou lorsque le curseur du panneau de configuration est utilisé pour modifier la résolution.</span><span class="sxs-lookup"><span data-stu-id="f1f47-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="f1f47-139">La mise à l’échelle dans le système d’exploitation peut entraîner un flou des applications WPF, en particulier lorsque la mise à l’échelle est non intégrale.</span><span class="sxs-lookup"><span data-stu-id="f1f47-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="f1f47-140">Afin d’éviter la mise à l’échelle des applications WPF, vous devez les mettre à jour pour qu’elles prennent en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="f1f47-141">Exemple de procédure pas à pas pour chaque moniteur WPF</span><span class="sxs-lookup"><span data-stu-id="f1f47-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="f1f47-142">L' [exemple WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) avec prise en charge de l’analyse est un exemple d’application WPF mis à jour pour prendre en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="f1f47-143">Cet exemple est composé de deux projets :</span><span class="sxs-lookup"><span data-stu-id="f1f47-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="f1f47-144">NativeHelpers. vcxproj : il s’agit d’un projet d’assistance natif qui implémente la fonctionnalité de base permettant à une application WPF de prendre en charge la résolution par moniteur en utilisant les Win32APIs ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f1f47-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="f1f47-145">Le projet contient deux classes :</span><span class="sxs-lookup"><span data-stu-id="f1f47-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="f1f47-146">PerMonDPIHelpers : classe qui fournit des fonctions d’assistance pour les opérations liées à DPI, telles que la récupération de la valeur PPP actuelle de l’analyseur actif, la définition d’un processus pour la prise en charge DPI par moniteur, etc.</span><span class="sxs-lookup"><span data-stu-id="f1f47-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="f1f47-147">PerMonitorDPIWindow : classe de base dérivée de **System. Windows. Window** qui implémente les fonctionnalités permettant à une fenêtre d’application WPF d’être compatible avec la résolution par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="f1f47-148">Ajuste la taille de la fenêtre, la taille de rendu graphique et la taille de police en fonction des PPP du moniteur plutôt que de la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="f1f47-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="f1f47-149">WPFApplication. csproj : exemple d’application WPF qui utilise PerMonitorDPIWindow (PerMonitorDPIWindow) et montre comment la fenêtre d’application et le rendu se redimensionne quand la fenêtre est déplacée vers un moniteur avec une résolution différente ou lorsque le curseur dans le panneau de configuration d’affichage est utilisé pour modifier la résolution.</span><span class="sxs-lookup"><span data-stu-id="f1f47-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="f1f47-150">Pour exécuter l’exemple, suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f1f47-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="f1f47-151">Télécharger et décompresser l' [exemple WPF avec prise en charge par moniteur](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span><span class="sxs-lookup"><span data-stu-id="f1f47-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="f1f47-152">Démarrez Microsoft Visual Studio et sélectionnez **fichier > ouvrir > projet/solution**</span><span class="sxs-lookup"><span data-stu-id="f1f47-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="f1f47-153">Accédez au répertoire qui contient l’exemple décompressé.</span><span class="sxs-lookup"><span data-stu-id="f1f47-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="f1f47-154">Accédez au répertoire nommé pour l’exemple, puis double-cliquez sur le fichier de solution Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="f1f47-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="f1f47-155">Appuyez sur F7 ou utilisez **générer > générer la solution** pour générer l’exemple</span><span class="sxs-lookup"><span data-stu-id="f1f47-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="f1f47-156">Appuyez sur CTRL + F5 ou utilisez l' **> de débogage exécuter sans débogage** pour exécuter l’exemple</span><span class="sxs-lookup"><span data-stu-id="f1f47-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="f1f47-157">Pour voir l’impact de la modification du DPI sur une application WPF mise à jour pour être compatible avec la résolution PPP par moniteur à l’aide de la classe de base de l’exemple, déplacez la fenêtre d’application vers et depuis les affichages ayant des DPI différents.</span><span class="sxs-lookup"><span data-stu-id="f1f47-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="f1f47-158">Lorsque la fenêtre est déplacée entre les analyses, la taille de la fenêtre et l’échelle de l’interface utilisateur sont mises à jour en fonction de la résolution de l’affichage à l’aide du système graphique Scalable de WPF, plutôt que d’être mises à l’échelle par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f1f47-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="f1f47-159">L’interface utilisateur de l’application est rendue en mode natif et n’apparaît pas floue.</span><span class="sxs-lookup"><span data-stu-id="f1f47-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="f1f47-160">Si vous n’avez pas deux affichages avec des PPP différents, modifiez la résolution en modifiant le curseur dans le panneau de configuration d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f1f47-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="f1f47-161">La modification du curseur et le fait de cliquer sur **appliquer** redimensionnent la fenêtre de l’application et mettent automatiquement à jour la mise à l’échelle de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1f47-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="f1f47-162">Mise à jour d’une application WPF existante pour qu’elle prenne en charge les DPI par moniteur à l’aide d’un projet d’assistance dans l’exemple WPF</span><span class="sxs-lookup"><span data-stu-id="f1f47-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="f1f47-163">Si vous disposez d’une application WPF existante et que vous souhaitez utiliser le projet d’assistance PPP de l’exemple pour la prise en charge de l’informatique en DPI, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f1f47-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="f1f47-164">Télécharger et décompresser l’exemple WPF avec prise en charge par moniteur</span><span class="sxs-lookup"><span data-stu-id="f1f47-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="f1f47-165">Démarrez Visual Studio et sélectionnez **fichier > ouvrir > projet/solution**</span><span class="sxs-lookup"><span data-stu-id="f1f47-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="f1f47-166">Accédez au répertoire qui contient une application WPF existante et double-cliquez sur le fichier de solution Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="f1f47-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="f1f47-167">Cliquez avec le bouton droit sur **Solution > ajouter > projet existant** ![ une capture d’écran qui illustre la sélection de menu Ajouter : projet existant](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="f1f47-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="f1f47-168">Dans la boîte de dialogue de sélection de fichier, accédez au répertoire qui contient l’exemple décompressé.</span><span class="sxs-lookup"><span data-stu-id="f1f47-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="f1f47-169">Ouvrez le répertoire nommé pour l’exemple, accédez au dossier « NativeHelpers », sélectionnez le fichier projet Visual C++ « NativeHelpers. vcxproj », puis cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="f1f47-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="f1f47-170">Cliquez avec le bouton droit sur le projet NativeHelpers et sélectionnez **générer**.</span><span class="sxs-lookup"><span data-stu-id="f1f47-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="f1f47-171">Cela génère NativeHelpers.dll qui sera ajouté en tant que référence à l’application WPF à l’étape suivante ![ une capture d’écran illustrant la sélection du menu Générer](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="f1f47-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="f1f47-172">Ajoutez une référence à NativeHelpers.dll à partir de votre application WPF.</span><span class="sxs-lookup"><span data-stu-id="f1f47-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="f1f47-173">Développez votre projet d’application WPF, cliquez avec le bouton droit sur **références** , puis cliquez sur **Ajouter une référence...**</span><span class="sxs-lookup"><span data-stu-id="f1f47-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="f1f47-174">Dans la boîte de dialogue qui s’affiche, développez la section **solution** .</span><span class="sxs-lookup"><span data-stu-id="f1f47-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="f1f47-175">Sous **projets**, sélectionnez NativeHelpers, puis cliquez sur **OK** pour ![ obtenir une capture d’écran illustrant la boîte de dialogue Resource Manager.](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="f1f47-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="f1f47-176">Développez votre projet d’application WPF, développez **Propriétés**, puis ouvrez **AssemblyInfo. cs**.</span><span class="sxs-lookup"><span data-stu-id="f1f47-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="f1f47-177">Apporter les ajouts suivants à AssemblyInfo. cs</span><span class="sxs-lookup"><span data-stu-id="f1f47-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="f1f47-178">Ajoutez une référence à System. Windows. Media dans la section de référence (à l’aide de System. Windows. Media ;)</span><span class="sxs-lookup"><span data-stu-id="f1f47-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="f1f47-179">Ajout de l’attribut DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )</span><span class="sxs-lookup"><span data-stu-id="f1f47-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![capture d’écran illustrant les propriétés supplémentaires](images/scrvs-image4.png)
10. <span data-ttu-id="f1f47-181">Hériter de la classe de fenêtre WPF principale de la classe de base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="f1f47-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="f1f47-182">Mettez à jour le fichier. cs de la fenêtre WPF principale afin d’hériter de la classe de base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="f1f47-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="f1f47-183">Ajoutez une référence à NativeHelpers dans la section de référence en ajoutant la ligne `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="f1f47-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="f1f47-184">Hériter de la classe de fenêtre principale de la classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="f1f47-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![une capture d’écran illustrant la référence c++](images/scrvs-image5.png)
    -   <span data-ttu-id="f1f47-186">Mettez à jour le fichier. XAML de la fenêtre WPF principale afin d’hériter de la classe de base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="f1f47-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="f1f47-187">Ajoutez une référence à NativeHelpers dans la section de référence en ajoutant la ligne `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="f1f47-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="f1f47-188">Hériter de la classe de fenêtre principale de la classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="f1f47-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![capture d’écran illustrant l’ajout de la référence. Xaml](images/scrvs-image6.png)
11. <span data-ttu-id="f1f47-190">Appuyez sur F7 ou utilisez **générer > générer la solution** pour générer l’exemple</span><span class="sxs-lookup"><span data-stu-id="f1f47-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="f1f47-191">Appuyez sur CTRL + F5 ou utilisez l' **> de débogage exécuter sans débogage** pour exécuter l’exemple</span><span class="sxs-lookup"><span data-stu-id="f1f47-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="f1f47-192">L' [exemple](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) d’application WPF avec prise en charge de l’analyse illustre la manière dont une application WPF peut être mise à jour pour être compatible avec la résolution PPP par moniteur en répondant à la notification de fenêtre [**WM \_ DPICHANGED**](wm-dpichanged.md) .</span><span class="sxs-lookup"><span data-stu-id="f1f47-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="f1f47-193">En réponse à la notification de fenêtre, l’exemple met à jour la transformation de mise à l’échelle utilisée par WPF en fonction de la valeur PPP actuelle du moniteur sur lequel la fenêtre est activée.</span><span class="sxs-lookup"><span data-stu-id="f1f47-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="f1f47-194">Le *wParam* de la notification de fenêtre contient la nouvelle PPP dans *wParam*.</span><span class="sxs-lookup"><span data-stu-id="f1f47-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="f1f47-195">Le *lParam* contient un rectangle qui a la taille et la position de la nouvelle fenêtre suggérée, mise à l’échelle pour la nouvelle résolution PPP.</span><span class="sxs-lookup"><span data-stu-id="f1f47-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="f1f47-196">Remarque :</span><span class="sxs-lookup"><span data-stu-id="f1f47-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="f1f47-197">Dans la mesure où cet exemple remplace la taille de la fenêtre et la transformation d’échelle du nœud racine de la fenêtre WPF, un travail supplémentaire peut être requis par le développeur d’applications dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="f1f47-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="f1f47-198">La taille de la fenêtre a un impact sur les autres parties de l’application, telles que la fenêtre WPF qui est hébergée dans une autre application.</span><span class="sxs-lookup"><span data-stu-id="f1f47-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="f1f47-199">L’application WPF qui étend cette classe définit d’autres transformations sur le visuel racine. l’exemple peut remplacer une autre transformation appliquée par l’application WPF elle-même.</span><span class="sxs-lookup"><span data-stu-id="f1f47-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="f1f47-200">Vue d’ensemble du projet d’assistance dans l’exemple WPF</span><span class="sxs-lookup"><span data-stu-id="f1f47-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="f1f47-201">Pour rendre une application WPF existante prenant en charge DPI par moniteur, la bibliothèque NativeHelpers fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1f47-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="f1f47-202">**Marque l’application WPF en fonction de la prise en charge DPI par ponitor :** L’application WPF est marquée comme prise en charge DPI par moniteur en appelant [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) pour le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="f1f47-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="f1f47-203">Le marquage de l’application en fonction de la prise en charge DPI par moniteur permet de garantir que</span><span class="sxs-lookup"><span data-stu-id="f1f47-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="f1f47-204">Le système d’exploitation n’effectue pas la mise à l’échelle de l’application lorsque la résolution du système ne correspond pas à la résolution actuelle de l’analyse de la fenêtre de l’application.</span><span class="sxs-lookup"><span data-stu-id="f1f47-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="f1f47-205">Le message [**WM \_ DPICHANGED**](wm-dpichanged.md) est envoyé à chaque modification de la résolution de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="f1f47-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="f1f47-206">**Ajuste la dimension de la fenêtre, redisposition et restitue à nouveau le contenu graphique et sélectionne les polices en fonction de la résolution initiale du moniteur sur lequel la fenêtre est activée :** Une fois que l’application est marquée avec la prise en charge DPI par moniteur, WPF met toujours à l’échelle la taille de la fenêtre, les graphiques et la taille de police en fonction de la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="f1f47-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="f1f47-207">Dans la mesure où, au lancement de l’application, il n’est pas garanti que la résolution des PPP du système soit identique à celle du moniteur sur lequel la fenêtre est lancée, la bibliothèque ajuste ces valeurs une fois la fenêtre chargée.</span><span class="sxs-lookup"><span data-stu-id="f1f47-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="f1f47-208">La classe de base **PerMonitorDPIWindow** les met à jour dans le gestionnaire **OnLoaded ()** .</span><span class="sxs-lookup"><span data-stu-id="f1f47-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="f1f47-209">La taille de la fenêtre est mise à jour en modifiant les propriétés de **largeur** et de **hauteur** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f1f47-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="f1f47-210">La disposition et la taille sont mises à jour en appliquant une transformation d’échelle appropriée au nœud racine de la fenêtre WPF.</span><span class="sxs-lookup"><span data-stu-id="f1f47-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="f1f47-211">**Répond à WM \_ Notification de fenêtre DPICHANGED :** mettez à jour la taille de la fenêtre, les graphiques et la taille de police en fonction des PPP passés dans la notification de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f1f47-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="f1f47-212">La classe de base **PerMonitorDPIWindow** gère la notification de fenêtre dans la méthode **HandleMessages ()** .</span><span class="sxs-lookup"><span data-stu-id="f1f47-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="f1f47-213">La taille de la fenêtre est mise à jour en appelant **SetWindowPos** à l’aide des informations passées dans le *lParam* du message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f1f47-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="f1f47-214">La disposition et la taille des graphiques sont mises à jour en appliquant une transformation d’échelle appropriée au nœud racine de la fenêtre WPF.</span><span class="sxs-lookup"><span data-stu-id="f1f47-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="f1f47-215">Le facteur d’échelle est calculé à l’aide du PPP passé dans le *wParam* du message de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f1f47-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="f1f47-216">Gestion de la modification DPI pour les ressources telles que les images</span><span class="sxs-lookup"><span data-stu-id="f1f47-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="f1f47-217">Pour mettre à jour le contenu graphique, l’exemple d’application WPF applique une transformation d’échelle au nœud racine de l’application WPF.</span><span class="sxs-lookup"><span data-stu-id="f1f47-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="f1f47-218">Bien que cela fonctionne bien pour le contenu qui est rendu en mode natif par WPF (Rectangle, texte, etc.), cela implique que les ressources bitmap comme les images sont mises à l’échelle par WPF.</span><span class="sxs-lookup"><span data-stu-id="f1f47-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="f1f47-219">Afin d’éviter les bitmaps floues provoqués par la mise à l’échelle, le développeur d’applications WPF peut écrire un contrôle d’image DPI personnalisé qui sélectionne une autre ressource en fonction de la valeur PPP actuelle du moniteur sur lequel se trouve la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f1f47-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="f1f47-220">Le contrôle image peut reposer sur l’événement **DPIChanged ()** déclenché pour la fenêtre WPF qui consomme à partir du **PerMonitorDPIWindow**, lorsque les PPP changent.</span><span class="sxs-lookup"><span data-stu-id="f1f47-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="f1f47-221">Le contrôle image doit également sélectionner le contrôle approprié pendant le lancement de l’application dans le gestionnaire d’événements de fenêtre WPF **chargé ()** .</span><span class="sxs-lookup"><span data-stu-id="f1f47-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 
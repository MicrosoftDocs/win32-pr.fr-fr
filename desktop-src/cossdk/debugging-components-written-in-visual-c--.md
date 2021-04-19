---
description: Lorsque vous êtes prêt à déboguer la fonctionnalité COM+ dans vos composants Microsoft Visual C++, vous pouvez configurer Visual C++ projet ou l’outil d’administration Services de composants pour lancer le débogueur.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Débogage de composants écrits en Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516770"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="3fb82-103">Débogage de composants écrits en Visual C++</span><span class="sxs-lookup"><span data-stu-id="3fb82-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="3fb82-104">Lorsque vous êtes prêt à déboguer la fonctionnalité COM+ dans vos composants Microsoft Visual C++, vous pouvez configurer Visual C++ projet ou l’outil d’administration Services de composants pour lancer le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="3fb82-105">Si vous utilisez Visual C++, vous pouvez déboguer avec un client distant en utilisant OLE RPC et le débogage juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="3fb82-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="3fb82-106">Si vous ne parvenez pas à exécuter votre client sous le débogueur ou si le client s’exécute sur un autre ordinateur, vous pouvez utiliser le paramètre **de lancement de com+ dans le débogueur** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="3fb82-107">Vous le trouverez dans l’outil d’administration Services de composants comme une case à cocher sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="3fb82-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="3fb82-108">Lorsque vous avez terminé le débogage, vous devez arrêter les applications COM+ que vous déboguez.</span><span class="sxs-lookup"><span data-stu-id="3fb82-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="3fb82-109">Si un processus serveur est en cours d’exécution, vous pouvez recevoir un message d’erreur la prochaine fois que vous essaierez de générer une DLL lorsque la DLL existante sera encore chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fb82-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="3fb82-110">Pour arrêter une application COM+, cliquez avec le bouton droit sur l’application dans l’arborescence de la console, puis cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="3fb82-111">Si vous utilisez des transactions, vous pouvez également augmenter le délai d’expiration de la transaction, qui est par défaut de 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="3fb82-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="3fb82-112">Vous pouvez également spécifier la valeur 0, en spécifiant un délai d’expiration de transaction infini.</span><span class="sxs-lookup"><span data-stu-id="3fb82-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="3fb82-113">À l’aide de l’outil d’administration Services de composants, modifiez le paramètre de délai d’expiration de la transaction sous l’onglet **options** de la fenêtre **Propriétés du poste de travail** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="3fb82-114">Débogage des composants d’application serveur avec Visual C++</span><span class="sxs-lookup"><span data-stu-id="3fb82-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="3fb82-115">Lors du débogage d’applications serveur COM+, vous pouvez déboguer des appels distants en chargeant le client et l’application serveur dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="3fb82-116">Avec Visual C++, vous pouvez déboguer des appels distants à vos composants via les paramètres JIT (Just-in-Time) et OLE RPC.</span><span class="sxs-lookup"><span data-stu-id="3fb82-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="3fb82-117">Le paramètre JIT fait en sorte que le composant compilé démarre le débogueur Visual C++ lorsqu’une erreur se produit ; le paramètre OLE RPC permet au débogueur d’effectuer un pas à pas du client au composant à mesure que vous parcourez votre code.</span><span class="sxs-lookup"><span data-stu-id="3fb82-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="3fb82-118">Lorsque ces fonctionnalités sont activées, vous pouvez démarrer votre client sous le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="3fb82-119">Lorsque le client effectue un appel à votre composant, le débogueur effectue un pas à pas détaillé dans le code du composant dans le processus serveur, même si le serveur se trouve sur un autre ordinateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="3fb82-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="3fb82-120">Une session de débogage est automatiquement démarrée sur l’ordinateur serveur, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3fb82-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="3fb82-121">De même, l’exécution pas à pas unique de l’instruction return dans le code du composant retourne le débogage à l’instruction suivante dans le code du client.</span><span class="sxs-lookup"><span data-stu-id="3fb82-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="3fb82-122">Vous pourrez peut-être enregistrer quelques étapes à l’aide du paramètre **de lancement de com+ dans le débogueur** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="3fb82-123">Cela vous permet de spécifier le débogueur Visual C++ (ou autre) sans avoir à définir des paramètres de débogage spéciaux dans l’environnement Visual C++.</span><span class="sxs-lookup"><span data-stu-id="3fb82-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="3fb82-124">Vous le trouverez dans l’outil d’administration Services de composants comme une case à cocher sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="3fb82-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="3fb82-125">Pour plus d’informations, consultez « Débogage sans Visual C++ » dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3fb82-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="3fb82-126">Lorsque l’application COM+ contenant votre composant est une application serveur, vous devez commencer par arrêter l’application à l’aide de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="3fb82-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="3fb82-127">Pour ce faire, cliquez avec le bouton droit sur l’application COM+ dans l’arborescence de la console, puis cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="3fb82-128">**Pour activer le débogage RPC dans Visual C++**</span><span class="sxs-lookup"><span data-stu-id="3fb82-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="3fb82-129">Dans Visual C++, dans le menu **Outils** , cliquez sur **options**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="3fb82-130">Dans la boîte de dialogue **options** , sous l’onglet **Déboguer** , activez les cases à cocher débogage **OLE RPC** et **débogage juste-à-temps** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="3fb82-131">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-131">Click **OK**.</span></span>

<span data-ttu-id="3fb82-132">Pour commencer le débogage, démarrez votre projet client dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="3fb82-133">Vous pouvez également déboguer votre composant sans lancer votre client dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="3fb82-134">Dans ce cas, votre composant doit lancer le débogueur seul.</span><span class="sxs-lookup"><span data-stu-id="3fb82-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="3fb82-135">Pour ce faire, votre projet de composant doit spécifier un fichier exécutable pour la session de débogage, ainsi que l’ID de l’application COM+.</span><span class="sxs-lookup"><span data-stu-id="3fb82-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="3fb82-136">**Pour permettre à un composant d’application serveur de lancer le débogueur Visual C++**</span><span class="sxs-lookup"><span data-stu-id="3fb82-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="3fb82-137">Dans le menu **projet** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="3fb82-138">Dans la boîte de dialogue **paramètres du projet** , dans la zone **paramètres pour** , sélectionnez **débogage Win32**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="3fb82-139">Sous l’onglet **Déboguer** , dans la zone **catégorie** , sélectionnez **général**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="3fb82-140">Dans la zone **exécutable pour la session de débogage** , entrez le chemin d’accès complet de Dllhost.exe, suivi d’un argument spécifiant l’ID d’application de l’application com+ contenant le composant.</span><span class="sxs-lookup"><span data-stu-id="3fb82-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="3fb82-141">À l’aide de l’outil d’administration Services de composants, vous trouverez l’ID de l’application sous l’onglet **général** de la boîte de dialogue **Propriétés** de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="3fb82-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="3fb82-142">Vous trouverez ci-dessous un exemple :</span><span class="sxs-lookup"><span data-stu-id="3fb82-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="3fb82-143">C : \\ winnt winnt \\ \\Dllhost.exe/ProcessId : {ApplicationId}</span><span class="sxs-lookup"><span data-stu-id="3fb82-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="3fb82-144">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-144">Click **OK**.</span></span>

<span data-ttu-id="3fb82-145">Vous pouvez maintenant définir des points d’arrêt, démarrer le débogueur et commencer à effectuer des appels à votre composant.</span><span class="sxs-lookup"><span data-stu-id="3fb82-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="3fb82-146">Débogage des composants d’application de la bibliothèque avec Visual C++</span><span class="sxs-lookup"><span data-stu-id="3fb82-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="3fb82-147">Pour déboguer des composants dans une application de bibliothèque, vous devez configurer le projet du client, car le processus du client hébergera l’application de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3fb82-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="3fb82-148">**Pour activer le débogage d’application de bibliothèque avec Visual C++**</span><span class="sxs-lookup"><span data-stu-id="3fb82-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="3fb82-149">Dans Visual C++, dans le menu **projet** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="3fb82-150">Dans la boîte de dialogue **paramètres du projet** , dans la zone **paramètres pour** , cliquez sur **débogage Win32**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="3fb82-151">Sous l’onglet **Déboguer** , dans la zone **catégorie** , cliquez sur **autres dll**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="3fb82-152">Dans la liste **modules** , ajoutez les dll du composant dans votre application de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3fb82-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="3fb82-153">Cela vous permet de définir des points d’arrêt avant le chargement de votre DLL.</span><span class="sxs-lookup"><span data-stu-id="3fb82-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="3fb82-154">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="3fb82-155">Débogage sans Visual C++</span><span class="sxs-lookup"><span data-stu-id="3fb82-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="3fb82-156">Que vous utilisiez Visual C++ pour le débogage, vous pouvez utiliser le paramètre **lancer dans le débogueur** pour spécifier le débogueur dans lequel vos composants doivent s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3fb82-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="3fb82-157">**Pour spécifier un débogueur à partir de l’outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="3fb82-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="3fb82-158">Dans l’arborescence de la console, sélectionnez l’application de bibliothèque COM+ contenant les composants que vous souhaitez déboguer.</span><span class="sxs-lookup"><span data-stu-id="3fb82-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="3fb82-159">Cliquez avec le bouton droit sur l’application, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="3fb82-160">Dans la boîte de dialogue **Propriétés** de l’application, cliquez sur l’onglet **avancé** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="3fb82-161">Sous **débogage**, activez la case à cocher **lancer dans le débogueur** .</span><span class="sxs-lookup"><span data-stu-id="3fb82-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="3fb82-162">Dans la zone **chemin du débogueur** , entrez le chemin d’accès au débogueur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="3fb82-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="3fb82-163">Vous pouvez également cliquer sur **Parcourir** pour rechercher le débogueur.</span><span class="sxs-lookup"><span data-stu-id="3fb82-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="3fb82-164">Voici un exemple : C : \\ winnt \\ system32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="3fb82-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="3fb82-165">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb82-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fb82-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fb82-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb82-167">Débogage de composants écrits en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3fb82-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 




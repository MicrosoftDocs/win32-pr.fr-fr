---
title: Dépannage des applications
description: Cette section fournit des solutions aux problèmes courants.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Applications tactiles Windows, résolution des problèmes
- Tactile Windows, rejet de Palm
- rejet de Palm
- Tactile Windows, support hérité
- Dépannage de Windows Touch
- inertie, dépannage des applications
- manipulations, résolution des problèmes des applications
- mouvements, dépannage des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953522"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="208c4-111">Dépannage des applications</span><span class="sxs-lookup"><span data-stu-id="208c4-111">Troubleshooting Applications</span></span>

<span data-ttu-id="208c4-112">Cette section fournit des solutions aux problèmes courants.</span><span class="sxs-lookup"><span data-stu-id="208c4-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="208c4-113">Résolution de problèmes générale</span><span class="sxs-lookup"><span data-stu-id="208c4-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-114">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-114">Issue</span></span>    | <span data-ttu-id="208c4-115">J’exécute Windows Server 2008 et les fonctionnalités tactiles de Windows ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="208c4-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="208c4-116">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-116">Cause</span></span>    | <span data-ttu-id="208c4-117">Vous n’avez pas activé l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="208c4-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="208c4-118">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-118">Solution</span></span> | <span data-ttu-id="208c4-119">Ouvrez l’outil d’administration Gestionnaire de serveur : cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **Gestionnaire de serveur**.</span><span class="sxs-lookup"><span data-stu-id="208c4-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="208c4-120">Cliquez sur l’élément **fonctionnalités** dans la colonne de gauche.</span><span class="sxs-lookup"><span data-stu-id="208c4-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="208c4-121">Cliquez sur **Ajouter des fonctionnalités** dans la section **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="208c4-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="208c4-122">Sélectionnez **expérience utilisateur**, cliquez sur **suivant**, puis sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="208c4-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-123">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-123">Issue</span></span>    | <span data-ttu-id="208c4-124">Chaque fois que je déplace mon doigt rapidement sur mon application, une flèche s’affiche et mon geste ou manipulation ne s’inscrit pas correctement.</span><span class="sxs-lookup"><span data-stu-id="208c4-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="208c4-125">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-125">Cause</span></span>    | <span data-ttu-id="208c4-126">Les raccourcis sont activés lorsque vous n’en avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="208c4-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="208c4-127">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-127">Solution</span></span> | <span data-ttu-id="208c4-128">Les raccourcis sont activés lorsque vous souhaitez qu’ils soient désactivés.</span><span class="sxs-lookup"><span data-stu-id="208c4-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="208c4-129">Pour plus d’informations sur la désactivation des raccourcis stylet, consultez [prise en charge héritée du panorama avec des barres de défilement](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208c4-130">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-130">Issue</span></span></td>
<td><span data-ttu-id="208c4-131">Je ne peux pas discerner les entrées de souris et les entrées tactiles Windows.</span><span class="sxs-lookup"><span data-stu-id="208c4-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="208c4-132">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-132">Cause</span></span></td>
<td><span data-ttu-id="208c4-133">Windows génère des messages de souris pour la prise en charge héritée lorsqu’un utilisateur clique sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="208c4-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="208c4-134">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-134">Solution</span></span></td>
<td><span data-ttu-id="208c4-135">Vous pouvez appeler <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> pour les messages <strong>WM_LBUTTONDOWN</strong> et <strong>WM_LBUTTONUP</strong> afin de déterminer la source.</span><span class="sxs-lookup"><span data-stu-id="208c4-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="208c4-136">Le code suivant illustre cette opération.</span><span class="sxs-lookup"><span data-stu-id="208c4-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208c4-137">C++</span><span class="sxs-lookup"><span data-stu-id="208c4-137">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-138">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-138">Issue</span></span>    | <span data-ttu-id="208c4-139">Comment faire exécuter des applications Microsoft PixelSense sur Windows 7 ?</span><span class="sxs-lookup"><span data-stu-id="208c4-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="208c4-140">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-140">Cause</span></span>    | <span data-ttu-id="208c4-141">Windows Touch et Microsoft PixelSense sont incompatibles.</span><span class="sxs-lookup"><span data-stu-id="208c4-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="208c4-142">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-142">Solution</span></span> | <span data-ttu-id="208c4-143">Vous devez soit cibler la plateforme Windows 7, soit la plate-forme Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="208c4-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="208c4-144">Dépannage des manipulations et de l’inertie</span><span class="sxs-lookup"><span data-stu-id="208c4-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-145">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-145">Issue</span></span>    | <span data-ttu-id="208c4-146">Mon application est figée sans raison.</span><span class="sxs-lookup"><span data-stu-id="208c4-146">My application is freezing for no reason.</span></span> <span data-ttu-id="208c4-147">J’obtiens des violations d’accès quand j’Initialise mes interfaces d’objet.</span><span class="sxs-lookup"><span data-stu-id="208c4-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="208c4-148">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-148">Cause</span></span>    | <span data-ttu-id="208c4-149">Appel à **CoInitialize** manquant lors de l’utilisation des interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) ou [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="208c4-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="208c4-150">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-150">Solution</span></span> | <span data-ttu-id="208c4-151">Cela peut être dû à l’instanciation des objets COM (Component Object Model) Windows sans appeler CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="208c4-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="208c4-152">Cela se produit parfois quand vous convertissez des projets à l’aide de gestes à l’aide des manipulations ou des interfaces d’inertie.</span><span class="sxs-lookup"><span data-stu-id="208c4-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-153">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-153">Issue</span></span>    | <span data-ttu-id="208c4-154">Mon objet est incorrectement pivoté lorsqu’il est en cours de traduction.</span><span class="sxs-lookup"><span data-stu-id="208c4-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="208c4-155">La rotation à un seul doigt ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="208c4-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="208c4-156">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-156">Cause</span></span>    | <span data-ttu-id="208c4-157">Paramétrage incorrect des pivots sur un objet.</span><span class="sxs-lookup"><span data-stu-id="208c4-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="208c4-158">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-158">Solution</span></span> | <span data-ttu-id="208c4-159">Vous ne configurez pas correctement les points pivot de manipulation.</span><span class="sxs-lookup"><span data-stu-id="208c4-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="208c4-160">Définissez les propriétés [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) et [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) au centre de l’objet ou du point autour duquel vous souhaitez faire pivoter et définissez la propriété [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) sur le rayon de votre objet.</span><span class="sxs-lookup"><span data-stu-id="208c4-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="208c4-161">Dépannage des entrées tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="208c4-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-162">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-162">Issue</span></span>    | <span data-ttu-id="208c4-163">Après avoir traité le message [**WM \_ Touch**](wm-touchdown.md) , je cesse d’obtenir des commentaires sur les limites.</span><span class="sxs-lookup"><span data-stu-id="208c4-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="208c4-164">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-164">Cause</span></span>    | <span data-ttu-id="208c4-165">Consommation du message [**WM \_ Touch**](wm-touchdown.md) sans le gérer.</span><span class="sxs-lookup"><span data-stu-id="208c4-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="208c4-166">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-166">Solution</span></span> | <span data-ttu-id="208c4-167">Vous consommerez probablement un message tactile Windows sans le transférer à **DefWindowProc**, ce qui entraînera un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="208c4-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="208c4-168">Pour plus d’informations sur la façon de gérer correctement les messages [**WM \_ Touch**](wm-touchdown.md) , consultez [prise en main avec des messages tactiles Windows](getting-started-with-multi-touch-messages.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208c4-169">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-169">Issue</span></span></td>
<td><span data-ttu-id="208c4-170">J’inclut Windows. h, mais il dit toujours que <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="208c4-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="208c4-171">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-171">Cause</span></span></td>
<td><span data-ttu-id="208c4-172">La version de Windows dans Targetver. h est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="208c4-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="208c4-173">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-173">Solution</span></span></td>
<td><span data-ttu-id="208c4-174">Vous n’avez pas défini la version correcte de Windows dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="208c4-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="208c4-175">Le code suivant illustre les versions Windows correctement définies pour Windows Touch dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="208c4-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208c4-176">C++</span><span class="sxs-lookup"><span data-stu-id="208c4-176">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208c4-177">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-177">Issue</span></span></td>
<td><span data-ttu-id="208c4-178">Les coordonnées x et y de mes entrées tactiles semblent non valides.</span><span class="sxs-lookup"><span data-stu-id="208c4-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="208c4-179">Il s’agit de valeurs supérieures à celles attendues ou de valeurs négatives.</span><span class="sxs-lookup"><span data-stu-id="208c4-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="208c4-180">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-180">Cause</span></span></td>
<td><span data-ttu-id="208c4-181">Vous devrez peut-être convertir vos points tactiles en pixels, ou vous devrez peut-être convertir les coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="208c4-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="208c4-182">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-182">Solution</span></span></td>
<td><span data-ttu-id="208c4-183">Assurez-vous que vous appelez <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> et <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="208c4-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="208c4-184">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="208c4-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208c4-185">C++</span><span class="sxs-lookup"><span data-stu-id="208c4-185">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="208c4-186">Pour pouvoir utiliser la fonction <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> , vous devez disposer d’une prise en charge des résolutions élevées dans votre application.</span><span class="sxs-lookup"><span data-stu-id="208c4-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="208c4-187">Pour plus d’informations sur la prise en charge des résolutions élevées, visitez la section <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">haute résolution</a> de MSDN.</span><span class="sxs-lookup"><span data-stu-id="208c4-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-188">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-188">Issue</span></span>    | <span data-ttu-id="208c4-189">Je ne vois pas les messages [**WM \_ Touch**](wm-touchdown.md) , mais je sais que la touche Windows fonctionne parce que je vois les messages de [**\_ mouvement WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="208c4-190">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-190">Cause</span></span>    | <span data-ttu-id="208c4-191">Appel à [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)manquant.</span><span class="sxs-lookup"><span data-stu-id="208c4-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="208c4-192">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-192">Solution</span></span> | <span data-ttu-id="208c4-193">[**WM \_**](wm-touchdown.md) Les messages [**de \_ mouvement**](wm-gesture.md) tactile et WM s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="208c4-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="208c4-194">Si vous n’appelez pas [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous recevrez uniquement les messages de **\_ mouvement WM** .</span><span class="sxs-lookup"><span data-stu-id="208c4-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-195">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-195">Issue</span></span>    | <span data-ttu-id="208c4-196">Je remarque des petits retards à partir du moment où je touche mon doigt jusqu’au moment où j’obtiens une entrée dans mon application.</span><span class="sxs-lookup"><span data-stu-id="208c4-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="208c4-197">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-197">Cause</span></span>    | <span data-ttu-id="208c4-198">Le rejet de Palm entraîne des retards dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="208c4-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="208c4-199">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-199">Solution</span></span> | <span data-ttu-id="208c4-200">Si **TWF \_ WANTPALM** est défini dans les appels à [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), le rejet de Palm est activé.</span><span class="sxs-lookup"><span data-stu-id="208c4-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="208c4-201">Cela provoque un petit délai (de 100 ms) tandis que le logiciel teste si l’entrée provient d’un doigt, d’un stylet ou de la paume de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="208c4-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="208c4-202">Désactivez le rejet de Palm en appelant **RegisterTouchWindow** avec l’indicateur **TWF \_ WANTPALM** effacé.</span><span class="sxs-lookup"><span data-stu-id="208c4-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="208c4-203">Dépannage des gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="208c4-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-204">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-204">Issue</span></span>    | <span data-ttu-id="208c4-205">Une fois le message de [**\_ mouvement WM**](wm-gesture.md) géré, je cesse d’obtenir des commentaires sur les limites.</span><span class="sxs-lookup"><span data-stu-id="208c4-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="208c4-206">Ou bien, un geste qui fonctionnait précédemment ne fonctionne pas maintenant.</span><span class="sxs-lookup"><span data-stu-id="208c4-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="208c4-207">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-207">Cause</span></span>    | <span data-ttu-id="208c4-208">Consommation du message [**de \_ mouvement WM**](wm-gesture.md) sans le gérer.</span><span class="sxs-lookup"><span data-stu-id="208c4-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="208c4-209">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-209">Solution</span></span> | <span data-ttu-id="208c4-210">Vous consommerez probablement un message tactile Windows sans le transférer à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), ce qui entraînera un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="208c4-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="208c4-211">Pour plus d’informations sur la façon de gérer correctement les messages de [**\_ mouvement WM**](wm-gesture.md) , consultez [prise en main avec les gestes Windows](getting-started-with-multi-touch-gestures.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-212">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-212">Issue</span></span>    | <span data-ttu-id="208c4-213">Je ne vois pas les messages de [**\_ mouvement WM**](wm-gesture.md) , mais je sais que la touche Windows fonctionne, car je vois des messages [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="208c4-214">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-214">Cause</span></span>    | <span data-ttu-id="208c4-215">Appel de [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="208c4-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="208c4-216">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-216">Solution</span></span> | <span data-ttu-id="208c4-217">[**WM \_**](wm-touchdown.md) Les messages [**de \_ mouvement**](wm-gesture.md) tactile et WM s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="208c4-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="208c4-218">Si vous appelez [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous ne recevrez pas de messages de **\_ mouvement WM** .</span><span class="sxs-lookup"><span data-stu-id="208c4-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="208c4-219">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-219">Issue</span></span></td>
<td><span data-ttu-id="208c4-220">Je ne vois pas tous les mouvements que je m’attend à voir.</span><span class="sxs-lookup"><span data-stu-id="208c4-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="208c4-221">Par exemple, je vois des gestes avec l’identificateur <strong>GID_PAN</strong> mais pas <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="208c4-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="208c4-222">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-222">Cause</span></span></td>
<td><span data-ttu-id="208c4-223">Certains mouvements, tels que le mouvement de rotation, ne sont pas activés par défaut.</span><span class="sxs-lookup"><span data-stu-id="208c4-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="208c4-224">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-224">Solution</span></span></td>
<td><span data-ttu-id="208c4-225">Vous devez appeler <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> quand vous recevez un message de <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> comme décrit dans la référence <strong>WM_GESTURENOTIFY</strong> , ou vous devez ajouter un gestionnaire pour le message <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="208c4-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="208c4-226">Le code suivant montre comment implémenter un gestionnaire pour activer la prise en charge de la rotation.</span><span class="sxs-lookup"><span data-stu-id="208c4-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="208c4-227">C++</span><span class="sxs-lookup"><span data-stu-id="208c4-227">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="208c4-228">Pour obtenir plus d’exemples de configurations de mouvements typiques, consultez <strong>SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="208c4-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-229">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-229">Issue</span></span>    | <span data-ttu-id="208c4-230">Les barres de défilement personnalisées dans mon application ne défilent pas lorsque j’effectue le mouvement panoramique.</span><span class="sxs-lookup"><span data-stu-id="208c4-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="208c4-231">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-231">Cause</span></span>    | <span data-ttu-id="208c4-232">Gestionnaires manquants pour les messages de défilement WM corrects \_ \* .</span><span class="sxs-lookup"><span data-stu-id="208c4-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="208c4-233">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-233">Solution</span></span> | <span data-ttu-id="208c4-234">Vous ne gérez pas tous les messages de \_ \* défilement WM dans vos barres de défilement personnalisées.</span><span class="sxs-lookup"><span data-stu-id="208c4-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="208c4-235">Il est recommandé de gérer le message [**de \_ mouvement WM**](wm-gesture.md) plutôt que de conserver les fonctionnalités de la barre de défilement personnalisée via la prise en charge héritée.</span><span class="sxs-lookup"><span data-stu-id="208c4-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="208c4-236">Vous devez prendre en charge les messages comme détaillé dans la section [prise en charge héritée du panorama avec les barres de défilement](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="208c4-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c4-237">Problème</span><span class="sxs-lookup"><span data-stu-id="208c4-237">Issue</span></span>    | <span data-ttu-id="208c4-238">J’obtiens des retards pour les gestes.</span><span class="sxs-lookup"><span data-stu-id="208c4-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="208c4-239">Cause</span><span class="sxs-lookup"><span data-stu-id="208c4-239">Cause</span></span>    | <span data-ttu-id="208c4-240">Les raccourcis peuvent entraîner des retards pour les gestes.</span><span class="sxs-lookup"><span data-stu-id="208c4-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="208c4-241">Solution</span><span class="sxs-lookup"><span data-stu-id="208c4-241">Solution</span></span> | <span data-ttu-id="208c4-242">Les raccourcis peuvent entraîner des retards pendant le temps nécessaire à votre application pour recevoir des messages de [**\_ mouvement WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="208c4-243">Pour plus d’informations sur la désactivation des raccourcis, consultez [prise en charge de l’héritage pour le panoramique avec les barres de défilement](legacy-support-for-panning-with-scrollbars.md) .</span><span class="sxs-lookup"><span data-stu-id="208c4-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="208c4-244">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="208c4-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="208c4-245">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="208c4-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
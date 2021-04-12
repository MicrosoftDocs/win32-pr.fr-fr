---
title: Prise en main avec des messages tactiles Windows
description: Cette section explique les tâches associées à l’obtention de l’entrée tactile Windows pour fonctionner dans votre application.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Tactile Windows, messages
- Tactile Windows, inscription pour une entrée tactile
- Windows Touch, test des numériseurs d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382094"
---
# <a name="getting-started-with-windows-touch-messages"></a><span data-ttu-id="83e63-106">Prise en main avec des messages tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="83e63-106">Getting Started with Windows Touch Messages</span></span>

<span data-ttu-id="83e63-107">Cette section explique les tâches associées à l’obtention de l’entrée tactile Windows pour fonctionner dans votre application.</span><span class="sxs-lookup"><span data-stu-id="83e63-107">This section explains the tasks associated with getting Windows Touch input to function in your application.</span></span>

<span data-ttu-id="83e63-108">Les étapes suivantes sont généralement effectuées lors de l’utilisation de messages tactiles Windows :</span><span class="sxs-lookup"><span data-stu-id="83e63-108">The following steps are typically performed when working with Windows Touch messages:</span></span>

1.  <span data-ttu-id="83e63-109">Testez les fonctionnalités du digitaliseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-109">Test the capabilities of the input digitizer.</span></span>
2.  <span data-ttu-id="83e63-110">Inscrivez-vous pour recevoir des messages tactiles Windows.</span><span class="sxs-lookup"><span data-stu-id="83e63-110">Register to receive Windows Touch messages.</span></span>
3.  <span data-ttu-id="83e63-111">Gérer les messages.</span><span class="sxs-lookup"><span data-stu-id="83e63-111">Handle the messages.</span></span>

<span data-ttu-id="83e63-112">Le message utilisé pour Windows Touch est [**WM \_ Touch**](wm-touchdown.md).</span><span class="sxs-lookup"><span data-stu-id="83e63-112">The message used for Windows Touch is [**WM\_TOUCH**](wm-touchdown.md).</span></span> <span data-ttu-id="83e63-113">Ce message indique les différents États de contact avec un digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="83e63-113">This message indicates the various states of contact with a digitizer.</span></span>

## <a name="testing-the-capabilities-of-the-input-digitizer"></a><span data-ttu-id="83e63-114">Test des fonctionnalités du digitaliseur d’entrée</span><span class="sxs-lookup"><span data-stu-id="83e63-114">Testing the Capabilities of the Input Digitizer</span></span>

<span data-ttu-id="83e63-115">La fonction [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) peut être utilisée pour interroger les fonctionnalités du digitaliseur d’entrée en passant la valeur *nIndex* du **\_ digitaliseur SM**.</span><span class="sxs-lookup"><span data-stu-id="83e63-115">The [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function can be used to query the capabilities of the input digitizer by passing in the *nIndex* value of **SM\_DIGITIZER**.</span></span> <span data-ttu-id="83e63-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retourne un champ de bits qui indique si l’appareil est prêt, si ce dernier prend en charge PEN ou Touch, si le périphérique d’entrée est intégré ou externe, et si l’appareil prend en charge plusieurs entrées (Windows Touch).</span><span class="sxs-lookup"><span data-stu-id="83e63-116">[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) returns a bit field that indicates whether the device is ready, whether the device supports pen or touch, whether the input device is integrated or external, and whether the device supports multiple inputs (Windows Touch).</span></span> <span data-ttu-id="83e63-117">Le tableau suivant présente les bits des différents champs.</span><span class="sxs-lookup"><span data-stu-id="83e63-117">The following table shows the bits for the various fields.</span></span>



| <span data-ttu-id="83e63-118">bit</span><span class="sxs-lookup"><span data-stu-id="83e63-118">Bit</span></span>   | <span data-ttu-id="83e63-119">8</span><span class="sxs-lookup"><span data-stu-id="83e63-119">8</span></span>           | <span data-ttu-id="83e63-120">7</span><span class="sxs-lookup"><span data-stu-id="83e63-120">7</span></span>           | <span data-ttu-id="83e63-121">6</span><span class="sxs-lookup"><span data-stu-id="83e63-121">6</span></span>        | <span data-ttu-id="83e63-122">5</span><span class="sxs-lookup"><span data-stu-id="83e63-122">5</span></span>        | <span data-ttu-id="83e63-123">4</span><span class="sxs-lookup"><span data-stu-id="83e63-123">4</span></span>            | <span data-ttu-id="83e63-124">3</span><span class="sxs-lookup"><span data-stu-id="83e63-124">3</span></span>              | <span data-ttu-id="83e63-125">2</span><span class="sxs-lookup"><span data-stu-id="83e63-125">2</span></span>              | <span data-ttu-id="83e63-126">1</span><span class="sxs-lookup"><span data-stu-id="83e63-126">1</span></span>                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| <span data-ttu-id="83e63-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="83e63-127">Value</span></span> | <span data-ttu-id="83e63-128">Pile prête</span><span class="sxs-lookup"><span data-stu-id="83e63-128">Stack Ready</span></span> | <span data-ttu-id="83e63-129">Entrée multiple</span><span class="sxs-lookup"><span data-stu-id="83e63-129">Multi-input</span></span> | <span data-ttu-id="83e63-130">Réservé</span><span class="sxs-lookup"><span data-stu-id="83e63-130">Reserved</span></span> | <span data-ttu-id="83e63-131">Réservé</span><span class="sxs-lookup"><span data-stu-id="83e63-131">Reserved</span></span> | <span data-ttu-id="83e63-132">Stylet externe</span><span class="sxs-lookup"><span data-stu-id="83e63-132">External Pen</span></span> | <span data-ttu-id="83e63-133">Stylet intégré</span><span class="sxs-lookup"><span data-stu-id="83e63-133">Integrated Pen</span></span> | <span data-ttu-id="83e63-134">Interaction tactile externe</span><span class="sxs-lookup"><span data-stu-id="83e63-134">External Touch</span></span> | <span data-ttu-id="83e63-135">Fonctions tactiles intégrées</span><span class="sxs-lookup"><span data-stu-id="83e63-135">Integrated Touch</span></span> |



 

<span data-ttu-id="83e63-136">Pour tester le résultat de la commande pour une fonctionnalité particulière, vous pouvez utiliser l’opérateur de & au niveau du bit et le bit particulier que vous testez.</span><span class="sxs-lookup"><span data-stu-id="83e63-136">To test the result from the command for a particular feature, you can use the bitwise & operator and the particular bit you are testing.</span></span> <span data-ttu-id="83e63-137">Par exemple, pour tester la fonction tactile Windows, vous devez vérifier que le bit septième ordre est défini (0x40 en hex).</span><span class="sxs-lookup"><span data-stu-id="83e63-137">For example, to test for Windows Touch, you would test that the seventh-order bit is set (0x40 in hex).</span></span> <span data-ttu-id="83e63-138">L’exemple de code suivant montre comment ces valeurs peuvent être testées.</span><span class="sxs-lookup"><span data-stu-id="83e63-138">The following code example shows how these values could be tested.</span></span>


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



<span data-ttu-id="83e63-139">Le tableau suivant répertorie les constantes définies dans Windows. h pour le test des fonctions tactiles du digitaliseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-139">The following table lists the constants defined in windows.h for testing touch capabilities of the input digitizer.</span></span>



| <span data-ttu-id="83e63-140">Nom</span><span class="sxs-lookup"><span data-stu-id="83e63-140">Name</span></span>                   | <span data-ttu-id="83e63-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="83e63-141">Value</span></span>      | <span data-ttu-id="83e63-142">Description</span><span class="sxs-lookup"><span data-stu-id="83e63-142">Description</span></span>                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e63-143">configuration de tablette \_ \_ aucune</span><span class="sxs-lookup"><span data-stu-id="83e63-143">TABLET\_CONFIG\_NONE</span></span>   | <span data-ttu-id="83e63-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="83e63-144">0x00000000</span></span> | <span data-ttu-id="83e63-145">Le digitaliseur d’entrée n’a pas de fonctionnalités tactiles.</span><span class="sxs-lookup"><span data-stu-id="83e63-145">The input digitizer does not have touch capabilities.</span></span>                                                                                                                                         |
| <span data-ttu-id="83e63-146">fonction \_ tactile intégrée nid \_</span><span class="sxs-lookup"><span data-stu-id="83e63-146">NID\_INTEGRATED\_TOUCH</span></span> | <span data-ttu-id="83e63-147">0x00000001</span><span class="sxs-lookup"><span data-stu-id="83e63-147">0x00000001</span></span> | <span data-ttu-id="83e63-148">Un digitaliseur tactile intégré est utilisé pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-148">An integrated touch digitizer is used for input.</span></span>                                                                                                                                              |
| <span data-ttu-id="83e63-149">\_ \_ interface tactile externe nid</span><span class="sxs-lookup"><span data-stu-id="83e63-149">NID\_EXTERNAL\_TOUCH</span></span>   | <span data-ttu-id="83e63-150">0x00000002</span><span class="sxs-lookup"><span data-stu-id="83e63-150">0x00000002</span></span> | <span data-ttu-id="83e63-151">Un digitaliseur tactile externe est utilisé pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-151">An external touch digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="83e63-152">\_ \_ stylet intégré nid</span><span class="sxs-lookup"><span data-stu-id="83e63-152">NID\_INTEGRATED\_PEN</span></span>   | <span data-ttu-id="83e63-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="83e63-153">0x00000004</span></span> | <span data-ttu-id="83e63-154">Un digitaliseur de stylet intégré est utilisé pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-154">An integrated pen digitizer is used for input.</span></span>                                                                                                                                                |
| <span data-ttu-id="83e63-155">\_ \_ stylet externe nid</span><span class="sxs-lookup"><span data-stu-id="83e63-155">NID\_EXTERNAL\_PEN</span></span>     | <span data-ttu-id="83e63-156">0x00000008</span><span class="sxs-lookup"><span data-stu-id="83e63-156">0x00000008</span></span> | <span data-ttu-id="83e63-157">Un digitaliseur de stylet externe est utilisé pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-157">An external pen digitizer is used for input.</span></span>                                                                                                                                                  |
| <span data-ttu-id="83e63-158">NID \_ multi- \_ entrée</span><span class="sxs-lookup"><span data-stu-id="83e63-158">NID\_MULTI\_INPUT</span></span>      | <span data-ttu-id="83e63-159">0x00000040</span><span class="sxs-lookup"><span data-stu-id="83e63-159">0x00000040</span></span> | <span data-ttu-id="83e63-160">Un digitaliseur d’entrée avec prise en charge de plusieurs entrées est utilisé pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-160">An input digitizer with support for multiple inputs is used for input.</span></span>                                                                                                                        |
| <span data-ttu-id="83e63-161">NID \_ prêt</span><span class="sxs-lookup"><span data-stu-id="83e63-161">NID\_READY</span></span>             | <span data-ttu-id="83e63-162">0x00000080</span><span class="sxs-lookup"><span data-stu-id="83e63-162">0x00000080</span></span> | <span data-ttu-id="83e63-163">Le digitaliseur d’entrée est prêt pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="83e63-163">The input digitizer is ready for input.</span></span> <span data-ttu-id="83e63-164">Si cette valeur est non définie, cela peut signifier que le service tablette est arrêté, que le digitaliseur n’est pas pris en charge ou que les pilotes du digitaliseur n’ont pas été installés.</span><span class="sxs-lookup"><span data-stu-id="83e63-164">If this value is unset, it may mean that the tablet service is stopped, the digitizer is not supported, or digitizer drivers have not been installed.</span></span> |



 

<span data-ttu-id="83e63-165">La vérification des \_ \* valeurs nid est un moyen utile de vérifier les capacités de l’ordinateur d’un utilisateur à configurer votre application pour l’entrée tactile, Pen ou non-tablette.</span><span class="sxs-lookup"><span data-stu-id="83e63-165">Checking the NID\_\* values is a useful way of checking the capabilities of a user's computer to configure your application for touch, pen, or non-tablet input.</span></span> <span data-ttu-id="83e63-166">Par exemple, si vous disposez d’une interface utilisateur dynamique et que vous souhaitez configurer automatiquement une partie de celle-ci, vous pouvez vérifier la valeur \_ tactile intégrée nid \_ , nid \_ tactile et peut obtenir le nombre maximal de touches à la première fois qu’un utilisateur exécute votre application.</span><span class="sxs-lookup"><span data-stu-id="83e63-166">For example, if you have a dynamic user interface (UI) and want to automatically configure some of it, you could check for NID\_INTEGRATED\_TOUCH, NID\_MULTITOUCH, and could get the maximum number of touches the first time that a user runs your application.</span></span>

> [!Note]  
> <span data-ttu-id="83e63-167">Il existe certaines limitations inhérentes à SM \_ GETSYSTEMMETRICS.</span><span class="sxs-lookup"><span data-stu-id="83e63-167">There are some inherent limitations for SM\_GETSYSTEMMETRICS.</span></span> <span data-ttu-id="83e63-168">Par exemple, le plug-and-Play n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="83e63-168">For example, there is no support for plug and play.</span></span> <span data-ttu-id="83e63-169">Pour cette raison, soyez prudent lors de l’utilisation de cette fonction comme moyen de configuration permanente.</span><span class="sxs-lookup"><span data-stu-id="83e63-169">For this reason, use caution when using this function as a means for permanent configuration.</span></span>

 

## <a name="registering-to-receive-windows-touch-input"></a><span data-ttu-id="83e63-170">Inscription pour recevoir des entrées tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="83e63-170">Registering to Receive Windows Touch Input</span></span>

<span data-ttu-id="83e63-171">Avant de recevoir des entrées tactiles Windows, les applications doivent d’abord s’inscrire pour recevoir des entrées tactiles Windows.</span><span class="sxs-lookup"><span data-stu-id="83e63-171">Before receiving Windows Touch input, applications must first register to receive Windows Touch input.</span></span> <span data-ttu-id="83e63-172">En inscrivant la fenêtre de l’application, l’application indique qu’elle est compatible avec le toucher.</span><span class="sxs-lookup"><span data-stu-id="83e63-172">By registering the application window, the application indicates that it is touch compatible.</span></span> <span data-ttu-id="83e63-173">Une fois que l’application a inscrit sa fenêtre, les notifications du pilote Windows Touch sont transférées à l’application lorsque l’entrée est effectuée dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="83e63-173">After the application registers its window, notifications from the Windows Touch driver are forwarded to the application when input is made on the window.</span></span> <span data-ttu-id="83e63-174">Lorsque l’application s’arrête, elle annule l’inscription de sa fenêtre pour désactiver les notifications.</span><span class="sxs-lookup"><span data-stu-id="83e63-174">When the application shuts down, it unregisters its window to disable notifications.</span></span>

> [!Note]  
> <span data-ttu-id="83e63-175">[**WM \_ Les messages TACTILEs**](wm-touchdown.md) sont actuellement « gourmands ».</span><span class="sxs-lookup"><span data-stu-id="83e63-175">[**WM\_TOUCH**](wm-touchdown.md) messages are currently "greedy."</span></span> <span data-ttu-id="83e63-176">Une fois le premier message tactile reçu dans une fenêtre, tous les messages tactiles sont envoyés à cette fenêtre jusqu’à ce qu’une autre fenêtre reçoive le focus.</span><span class="sxs-lookup"><span data-stu-id="83e63-176">After the first touch message is received on a window, all touch messages are sent to that window until another window receives focus.</span></span>

 

> [!Note]  
> <span data-ttu-id="83e63-177">Par défaut, vous recevez des messages de [**\_ mouvement WM**](wm-gesture.md) au lieu de messages [**WM \_ Touch**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="83e63-177">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages instead of [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="83e63-178">Si vous appelez [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous ne recevrez plus de messages de **\_ mouvement WM** .</span><span class="sxs-lookup"><span data-stu-id="83e63-178">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving **WM\_GESTURE** messages.</span></span>

 

<span data-ttu-id="83e63-179">Le code suivant montre comment une application peut s’inscrire pour recevoir des messages tactiles Windows dans une application Win32.</span><span class="sxs-lookup"><span data-stu-id="83e63-179">The following code demonstrates how an application could register to receive Windows Touch messages in a Win32 application.</span></span>


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a><span data-ttu-id="83e63-180">Gestion des messages tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="83e63-180">Handling Windows Touch Messages</span></span>

<span data-ttu-id="83e63-181">Vous pouvez gérer les messages tactiles Windows à partir d’applications dans les systèmes d’exploitation Windows de nombreuses façons.</span><span class="sxs-lookup"><span data-stu-id="83e63-181">You can handle the Windows Touch messages from applications in Windows operating systems in many ways.</span></span> <span data-ttu-id="83e63-182">Si vous programmez une application GUI, vous ajoutez du code dans la `WndProc` fonction pour gérer les messages qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="83e63-182">If you are programming a GUI application, you add code within the `WndProc` function to handle the messages of interest.</span></span> <span data-ttu-id="83e63-183">Si vous programmez une application MFC (Microsoft Foundation Class) ou une application managée, vous ajoutez des gestionnaires pour les messages qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="83e63-183">If you are programming a Microsoft Foundation Class (MFC) or managed application, you add handlers for the messages of interest.</span></span> <span data-ttu-id="83e63-184">L’exemple de code suivant montre comment les messages tactiles peuvent être gérés à partir de WndProc dans une application Windows.</span><span class="sxs-lookup"><span data-stu-id="83e63-184">The following code example shows how touch messages could be handled from WndProc in a Windows-based application.</span></span>


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





<span data-ttu-id="83e63-185">Le code suivant montre comment vous pouvez implémenter la table des messages et un gestionnaire de messages.</span><span class="sxs-lookup"><span data-stu-id="83e63-185">The following code shows how you can implement the message map and a message handler.</span></span> <span data-ttu-id="83e63-186">Notez que les messages doivent être déclarés dans la table des messages, puis que le gestionnaire du message doit être implémenté.</span><span class="sxs-lookup"><span data-stu-id="83e63-186">Note that the messages must be declared in the message map and then the handler for the message should be implemented.</span></span> <span data-ttu-id="83e63-187">Par exemple, dans une application MFC, elle peut être déclarée dans le code de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="83e63-187">For example, in an MFC application, this could be declared in the dialog code.</span></span> <span data-ttu-id="83e63-188">Notez également que la `OnInitDialog` fonction pour votre fenêtre de boîte de dialogue doit inclure un appel à [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , par exemple `RegisterTouchWindow(m_hWnd, 0)` .</span><span class="sxs-lookup"><span data-stu-id="83e63-188">Note also, that the `OnInitDialog` function for your dialog window would have to include a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) such as `RegisterTouchWindow(m_hWnd, 0)`.</span></span>


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



<span data-ttu-id="83e63-189">Le toucher de la fenêtre indique les touches à partir d’une fenêtre indépendante.</span><span class="sxs-lookup"><span data-stu-id="83e63-189">Touching the window will indicate touches from a pop-up window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83e63-190">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83e63-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e63-191">Entrée tactile Windows</span><span class="sxs-lookup"><span data-stu-id="83e63-191">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 
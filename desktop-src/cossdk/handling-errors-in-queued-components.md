---
description: Parfois, une situation se produit lorsqu’un message ne peut pas être remis à sa destination prévue, généralement en raison d’un problème au niveau du système ou de la configuration.
ms.assetid: 8015682c-d84d-44e2-995d-dca68053c4fa
title: Gestion des erreurs dans les composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95752adf82d74e39a9c93f1ae54584e72007f1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523871"
---
# <a name="handling-errors-in-queued-components"></a><span data-ttu-id="0d374-103">Gestion des erreurs dans les composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="0d374-103">Handling Errors in Queued Components</span></span>

<span data-ttu-id="0d374-104">Parfois, une situation se produit lorsqu’un message ne peut pas être remis à sa destination prévue, généralement en raison d’un problème au niveau du système ou de la configuration.</span><span class="sxs-lookup"><span data-stu-id="0d374-104">Occasionally, a situation occurs in which a message cannot be successfully delivered to its intended destination, usually due to a problem with the system or configuration.</span></span> <span data-ttu-id="0d374-105">Par exemple, le message peut être dirigé vers une file d’attente qui n’existe pas ou la file d’attente de destination n’est peut-être pas dans un État à recevoir.</span><span class="sxs-lookup"><span data-stu-id="0d374-105">For example, the message might be directed to a queue that does not exist or the destination queue might not be in a state to receive.</span></span> <span data-ttu-id="0d374-106">Le Data Mover est un outil qui déplace tous les messages d’échec [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) d’une file d’attente vers une autre, afin qu’ils puissent être retentés.</span><span class="sxs-lookup"><span data-stu-id="0d374-106">The message mover is a tool that moves all failed [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) messages from one queue to another so that they can be retried.</span></span> <span data-ttu-id="0d374-107">L’utilitaire de déplacement de messages est un objet Automation qui peut être appelé à l’aide d’un script VBScript.</span><span class="sxs-lookup"><span data-stu-id="0d374-107">The message mover utility is an Automation object that can be invoked with a VBScript.</span></span>

## <a name="components-services-administrative-tool"></a><span data-ttu-id="0d374-108">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="0d374-108">Components Services Administrative Tool</span></span>

<span data-ttu-id="0d374-109">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="0d374-109">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="0d374-110">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0d374-110">Visual Basic</span></span>

<span data-ttu-id="0d374-111">L’exemple de code suivant montre comment créer un objet MessageMover, définir les propriétés requises et initialiser le transfert.</span><span class="sxs-lookup"><span data-stu-id="0d374-111">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="0d374-112">Pour l’utiliser à partir de Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="0d374-112">To use it from Visual Basic, add a reference to the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="0d374-113">Pour utiliser l’objet MessageMover, vous devez disposer d’Message Queuing installé sur votre ordinateur et l’application spécifiée par AppName doit avoir activé la mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0d374-113">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="0d374-114">Pour plus d’informations sur l’installation de Message Queuing, consultez aide et support dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="0d374-114">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```VB
Function MyMessageMover( _
  strSource As String, _
  strDest As String _
) As Boolean  ' Return False if any errors occur.

    MyMessageMover = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim lngMovedMessages As Long
    Dim objMessageMover As COMSVCSLib.MessageMover
    Set objMessageMover = CreateObject("QC.MessageMover")
    objMessageMover.SourcePath = strSource
    objMessageMover.DestPath = strDest
    lngMovedMessages = objMessageMover.MoveMessages

    MsgBox lngMovedMessages & " messages moved from " & _
      strSource & " to " & strDest

    MyMessageMover = True  ' Successful end to procedure
    Set objMessageMover = Nothing
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objMessageMover = Nothing
    lngMovedMessages = -1
End Function

```



<span data-ttu-id="0d374-115">Le code Visual Basic suivant montre comment appeler la fonction MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="0d374-115">The following Visual Basic code shows how to call the MyMessageMover function.</span></span>


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



<span data-ttu-id="0d374-116">Le chemin d’accès source du message est la file d’attente Rest finale.</span><span class="sxs-lookup"><span data-stu-id="0d374-116">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="0d374-117">Il s’agit de la file d’attente morte, qui est une file d’attente de Message Queuing privée, appelée AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="0d374-117">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="0d374-118">Les messages sont déplacés ici si la transaction est abandonnée à plusieurs reprises lors de la nouvelle file d’attente de nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="0d374-118">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="0d374-119">Avec l’outil de déplacement de messages, vous pouvez replacer le message dans la première file d’attente, appelée AppName.</span><span class="sxs-lookup"><span data-stu-id="0d374-119">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="0d374-120">Pour plus d’informations sur les files d’attente de nouvelle tentative, consultez [Erreurs côté serveur](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-120">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="0d374-121">Si les attributs de file d’attente le permettent, le Data Mover déplace les messages de manière transitoire afin que les messages ne soient pas perdus ou dupliqués en cas de défaillance pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="0d374-121">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="0d374-122">L’outil conserve toutes les propriétés de message qui peuvent être conservées lors du déplacement des messages d’une file d’attente vers une autre.</span><span class="sxs-lookup"><span data-stu-id="0d374-122">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="0d374-123">Si les messages sont générés par des appels de composants en file d’attente COM+, l’utilitaire de déplacement de messages conserve l’identificateur de sécurité de l’appelant d’origine lorsqu’il déplace des messages entre les files d’attente.</span><span class="sxs-lookup"><span data-stu-id="0d374-123">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="0d374-124">Si les files d’attente source et de destination sont transactionnelles, l’intégralité de l’opération est effectuée de façon transitoire.</span><span class="sxs-lookup"><span data-stu-id="0d374-124">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="0d374-125">Si les files d’attente source ou de destination ne sont pas transactionnelles, l’opération ne s’exécute pas dans le cadre d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="0d374-125">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="0d374-126">Une défaillance inattendue (par exemple, un incident) et le redémarrage d’un déplacement non transactionnel peuvent dupliquer le message déplacé au moment de l’échec.</span><span class="sxs-lookup"><span data-stu-id="0d374-126">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="cc"></a><span data-ttu-id="0d374-127">C/C++</span><span class="sxs-lookup"><span data-stu-id="0d374-127">C/C++</span></span>

<span data-ttu-id="0d374-128">L’exemple de code suivant montre comment créer un objet MessageMover, définir les propriétés requises et initialiser le transfert.</span><span class="sxs-lookup"><span data-stu-id="0d374-128">The following sample code shows how to create a MessageMover object, set the required properties, and initiate the transfer.</span></span> <span data-ttu-id="0d374-129">La méthode ErrorDescription est décrite dans [interprétation des codes d’erreur](interpreting-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-129">The ErrorDescription method is described at [Interpreting Error Codes](interpreting-error-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="0d374-130">Pour utiliser l’objet MessageMover, vous devez disposer d’Message Queuing installé sur votre ordinateur et l’application spécifiée par AppName doit avoir activé la mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0d374-130">To use the MessageMover object, you must have Message Queuing installed on your computer and the application specified by AppName must have queuing enabled.</span></span> <span data-ttu-id="0d374-131">Pour plus d’informations sur l’installation de Message Queuing, consultez aide et support dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="0d374-131">For information about installing Message Queuing, see Help and Support on the **Start** menu.</span></span>

 


```C++
#include <windows.h>
#include <stdio.h>
#import "C:\WINDOWS\system32\ComSvcs.dll"
#include "ComSvcs.h"
#include "StrSafe.h"  

BOOL MyMessageMover (OLECHAR* szSource, OLECHAR* szDest) {
    IUnknown * pUnknown = NULL;
    IMessageMover * pMover = NULL;
    HRESULT hr = S_OK;
    BSTR bstrSource = NULL;
    BSTR bstrDest = NULL;
    unsigned int uMaxLen = 255;  // Maximum length of szMyApp

try {
    // Test the input strings to make sure they're OK to use.
    hr = StringCchLengthW(szSource, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    hr = StringCchLengthW(szDest, uMaxLen, NULL);
    if (FAILED (hr)) throw(hr);
    
    // Convert the input strings to BSTRs.
    bstrSource = SysAllocString(szSource);
    bstrDest = SysAllocString(szDest);

    // Create a MessageMover object and get its IUnknown.
    hr = CoCreateInstance(CLSID_MessageMover, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) throw(hr);    

    // Get the IMessageMover interface.
    hr = pUnknown->QueryInterface(IID_IMessageMover, (void**)&pMover); 
    if (FAILED (hr)) throw(hr);

    // Put the source and destination files.
    hr = pMover->put_SourcePath(bstrSource);
    if (FAILED (hr)) throw(hr);
    hr = pMover->put_DestPath(bstrDest);
    if (FAILED (hr)) throw(hr);

    // Move the messages.
    LONG lCount = -1;
    hr = pMover->MoveMessages(&lCount);
    if (FAILED (hr)) throw(hr);
    printf("%ld messages moved from %S to %S.\n", 
      lCount, bstrSource, bstrDest);

    // Clean up.
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    pUnknown->Release();
    pUnknown = NULL;
    pMover->Release();
    pMover = NULL;
    return (TRUE);
}  // try

catch(HRESULT hr) {  // Replace with specific error handling.
    printf("Error # %#x: ", hr);
    ErrorDescription(hr);
    SysFreeString(bstrDest);
    SysFreeString(bstrSource);
    if (NULL != pUnknown) pUnknown->Release();
    pUnknown = NULL;
    if (NULL != pMover) pMover->Release();
    pMover = NULL;
    return (FALSE);
}catch(...) {
    printf("An unexpected exception occurred.\n");
    throw;
}        
}  // MyMessageMover

```



<span data-ttu-id="0d374-132">Le code C++ suivant montre comment appeler la fonction MyMessageMover.</span><span class="sxs-lookup"><span data-stu-id="0d374-132">The following C++ code shows how to call the MyMessageMover function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define _WIN32_DCOM  // To use CoInitializeEx()

void main() 
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED (hr)) {
        printf("CoInitializeEx failed: Error # %#x\n", hr);
        exit(0);  // Replace with specific error handling.
    }
    if (! MyMessageMover(L".\\private$\\AppName_deadqueue", 
      L".\\AppName"))
        printf("MyMessageMover failed.\n");
    CoUninitialize();
}
```



<span data-ttu-id="0d374-133">Le chemin d’accès source du message est la file d’attente Rest finale.</span><span class="sxs-lookup"><span data-stu-id="0d374-133">The source path of the message is the final resting queue.</span></span> <span data-ttu-id="0d374-134">Il s’agit de la file d’attente morte, qui est une file d’attente de Message Queuing privée, appelée AppName \_ deadqueue.</span><span class="sxs-lookup"><span data-stu-id="0d374-134">It is the dead queue, which is a private Message Queuing queue and is called AppName\_deadqueue.</span></span> <span data-ttu-id="0d374-135">Les messages sont déplacés ici si la transaction est abandonnée à plusieurs reprises lors de la nouvelle file d’attente de nouvelles tentatives.</span><span class="sxs-lookup"><span data-stu-id="0d374-135">Messages are moved here if the transaction repeatedly aborts when attempted on the fifth retry queue.</span></span> <span data-ttu-id="0d374-136">Avec l’outil de déplacement de messages, vous pouvez replacer le message dans la première file d’attente, appelée AppName.</span><span class="sxs-lookup"><span data-stu-id="0d374-136">With the message mover tool, you can move the message back to the first queue, which is called AppName.</span></span> <span data-ttu-id="0d374-137">Pour plus d’informations sur les files d’attente de nouvelle tentative, consultez [Erreurs côté serveur](server-side-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0d374-137">For more information on retry queues, see [Server-Side Errors](server-side-errors.md).</span></span>

<span data-ttu-id="0d374-138">Si les attributs de file d’attente le permettent, le Data Mover déplace les messages de manière transitoire afin que les messages ne soient pas perdus ou dupliqués en cas de défaillance pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="0d374-138">If queue attributes permit, the message mover moves messages transitionally so that messages are not lost or duplicated in the event of failure during the move.</span></span> <span data-ttu-id="0d374-139">L’outil conserve toutes les propriétés de message qui peuvent être conservées lors du déplacement des messages d’une file d’attente vers une autre.</span><span class="sxs-lookup"><span data-stu-id="0d374-139">The tool preserves all the message properties that can be preserved when moving messages from one queue to another.</span></span>

<span data-ttu-id="0d374-140">Si les messages sont générés par des appels de composants en file d’attente COM+, l’utilitaire de déplacement de messages conserve l’identificateur de sécurité de l’appelant d’origine lorsqu’il déplace des messages entre les files d’attente.</span><span class="sxs-lookup"><span data-stu-id="0d374-140">If the messages are generated by COM+ Queued Components calls, the message mover utility preserves the original caller's security identifier as it moves messages between queues.</span></span> <span data-ttu-id="0d374-141">Si les files d’attente source et de destination sont transactionnelles, l’intégralité de l’opération est effectuée de façon transitoire.</span><span class="sxs-lookup"><span data-stu-id="0d374-141">If both the destination and source queues are transactional, the whole operation is done transitionally.</span></span> <span data-ttu-id="0d374-142">Si les files d’attente source ou de destination ne sont pas transactionnelles, l’opération ne s’exécute pas dans le cadre d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="0d374-142">If either the source or destination queues are not transactional, the operation does not run under a transaction.</span></span> <span data-ttu-id="0d374-143">Une défaillance inattendue (par exemple, un incident) et le redémarrage d’un déplacement non transactionnel peuvent dupliquer le message déplacé au moment de l’échec.</span><span class="sxs-lookup"><span data-stu-id="0d374-143">An unexpected failure (such as a crash) and restart of a non-transactional move could duplicate the message being moved at the time of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d374-144">Notes</span><span class="sxs-lookup"><span data-stu-id="0d374-144">Remarks</span></span>

<span data-ttu-id="0d374-145">COM+ gère les abandons côté serveur (joueur) en déplaçant le message qui échoue dans une file d’attente de « repos final » différente, afin de le récupérer.</span><span class="sxs-lookup"><span data-stu-id="0d374-145">COM+ handles server-side (player) aborts by moving the message that is failing onto a different "final resting" queue, to get it out of the way.</span></span> <span data-ttu-id="0d374-146">L’écouteur et le lecteur ne peuvent pas boucler continuellement sur un message qui s’interrompt.</span><span class="sxs-lookup"><span data-stu-id="0d374-146">The listener and player cannot continually loop on a message that aborts.</span></span> <span data-ttu-id="0d374-147">Dans de nombreux cas, la transaction abandonnée peut être corrigée en effectuant une action sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0d374-147">In many cases, the aborted transaction can be fixed by taking action at the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d374-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d374-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d374-149">Erreurs de composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="0d374-149">Queued Components Errors</span></span>](queued-components-errors.md)
</dt> </dl>

 

 




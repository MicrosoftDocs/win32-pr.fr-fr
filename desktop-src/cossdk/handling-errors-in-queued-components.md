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
# <a name="handling-errors-in-queued-components"></a>Gestion des erreurs dans les composants en file d’attente

Parfois, une situation se produit lorsqu’un message ne peut pas être remis à sa destination prévue, généralement en raison d’un problème au niveau du système ou de la configuration. Par exemple, le message peut être dirigé vers une file d’attente qui n’existe pas ou la file d’attente de destination n’est peut-être pas dans un État à recevoir. Le Data Mover est un outil qui déplace tous les messages d’échec [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) d’une file d’attente vers une autre, afin qu’ils puissent être retentés. L’utilitaire de déplacement de messages est un objet Automation qui peut être appelé à l’aide d’un script VBScript.

## <a name="components-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

L’exemple de code suivant montre comment créer un objet MessageMover, définir les propriétés requises et initialiser le transfert. Pour l’utiliser à partir de Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.

> [!Note]  
> Pour utiliser l’objet MessageMover, vous devez disposer d’Message Queuing installé sur votre ordinateur et l’application spécifiée par AppName doit avoir activé la mise en file d’attente. Pour plus d’informations sur l’installation de Message Queuing, consultez aide et support dans le menu **Démarrer** .

 


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



Le code Visual Basic suivant montre comment appeler la fonction MyMessageMover.


```VB
Sub Main()
  ' Replace AppName with the name of a COM+ application.
  If Not MyMessageMover(".\private$\AppName_deadqueue", ".\AppName") Then
      MsgBox "MyMessageMover failed."
  End If
End Sub

```



Le chemin d’accès source du message est la file d’attente Rest finale. Il s’agit de la file d’attente morte, qui est une file d’attente de Message Queuing privée, appelée AppName \_ deadqueue. Les messages sont déplacés ici si la transaction est abandonnée à plusieurs reprises lors de la nouvelle file d’attente de nouvelles tentatives. Avec l’outil de déplacement de messages, vous pouvez replacer le message dans la première file d’attente, appelée AppName. Pour plus d’informations sur les files d’attente de nouvelle tentative, consultez [Erreurs côté serveur](server-side-errors.md).

Si les attributs de file d’attente le permettent, le Data Mover déplace les messages de manière transitoire afin que les messages ne soient pas perdus ou dupliqués en cas de défaillance pendant le déplacement. L’outil conserve toutes les propriétés de message qui peuvent être conservées lors du déplacement des messages d’une file d’attente vers une autre.

Si les messages sont générés par des appels de composants en file d’attente COM+, l’utilitaire de déplacement de messages conserve l’identificateur de sécurité de l’appelant d’origine lorsqu’il déplace des messages entre les files d’attente. Si les files d’attente source et de destination sont transactionnelles, l’intégralité de l’opération est effectuée de façon transitoire. Si les files d’attente source ou de destination ne sont pas transactionnelles, l’opération ne s’exécute pas dans le cadre d’une transaction. Une défaillance inattendue (par exemple, un incident) et le redémarrage d’un déplacement non transactionnel peuvent dupliquer le message déplacé au moment de l’échec.

## <a name="cc"></a>C/C++

L’exemple de code suivant montre comment créer un objet MessageMover, définir les propriétés requises et initialiser le transfert. La méthode ErrorDescription est décrite dans [interprétation des codes d’erreur](interpreting-error-codes.md).

> [!Note]  
> Pour utiliser l’objet MessageMover, vous devez disposer d’Message Queuing installé sur votre ordinateur et l’application spécifiée par AppName doit avoir activé la mise en file d’attente. Pour plus d’informations sur l’installation de Message Queuing, consultez aide et support dans le menu **Démarrer** .

 


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



Le code C++ suivant montre comment appeler la fonction MyMessageMover.


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



Le chemin d’accès source du message est la file d’attente Rest finale. Il s’agit de la file d’attente morte, qui est une file d’attente de Message Queuing privée, appelée AppName \_ deadqueue. Les messages sont déplacés ici si la transaction est abandonnée à plusieurs reprises lors de la nouvelle file d’attente de nouvelles tentatives. Avec l’outil de déplacement de messages, vous pouvez replacer le message dans la première file d’attente, appelée AppName. Pour plus d’informations sur les files d’attente de nouvelle tentative, consultez [Erreurs côté serveur](server-side-errors.md).

Si les attributs de file d’attente le permettent, le Data Mover déplace les messages de manière transitoire afin que les messages ne soient pas perdus ou dupliqués en cas de défaillance pendant le déplacement. L’outil conserve toutes les propriétés de message qui peuvent être conservées lors du déplacement des messages d’une file d’attente vers une autre.

Si les messages sont générés par des appels de composants en file d’attente COM+, l’utilitaire de déplacement de messages conserve l’identificateur de sécurité de l’appelant d’origine lorsqu’il déplace des messages entre les files d’attente. Si les files d’attente source et de destination sont transactionnelles, l’intégralité de l’opération est effectuée de façon transitoire. Si les files d’attente source ou de destination ne sont pas transactionnelles, l’opération ne s’exécute pas dans le cadre d’une transaction. Une défaillance inattendue (par exemple, un incident) et le redémarrage d’un déplacement non transactionnel peuvent dupliquer le message déplacé au moment de l’échec.

## <a name="remarks"></a>Notes

COM+ gère les abandons côté serveur (joueur) en déplaçant le message qui échoue dans une file d’attente de « repos final » différente, afin de le récupérer. L’écouteur et le lecteur ne peuvent pas boucler continuellement sur un message qui s’interrompt. Dans de nombreux cas, la transaction abandonnée peut être corrigée en effectuant une action sur le serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreurs de composants en file d’attente](queued-components-errors.md)
</dt> </dl>

 

 




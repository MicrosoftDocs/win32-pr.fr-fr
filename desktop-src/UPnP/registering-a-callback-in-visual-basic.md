---
title: Inscription d’un rappel dans Visual Basic
description: L’ajout d’un rappel dans Visual Basic est différent de la méthode utilisée dans VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102049"
---
# <a name="registering-a-callback-in-visual-basic"></a>Inscription d’un rappel dans Visual Basic

L’ajout d’un rappel dans Visual Basic est différent de la méthode utilisée dans VBScript. La fonction **getRef** utilisée dans VBScript est différente de celle utilisée dans Visual Basic. Par conséquent, un développeur doit créer un objet [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui a la fonction de rappel comme méthode par défaut. Cette rubrique fournit les informations nécessaires pour développer des applications Visual Basic.

**Pour implémenter ce rappel dans une application**

1.  Ajoutez des références à deux bibliothèques d’objets : TLBTypes. olb et VboostTypes6. olb. Ces bibliothèques d’objets sont fournies avec l’exemple de code de point de contrôle.
2.  Ajoutez une référence à Cbklib. tlb. Ce fichier définit la structure de la fonction de rappel.

    Cbklib. tlb est créé à l’aide du fichier cbklib. idl inclus dans le cadre de l’exemple de code du point de contrôle. Il est recommandé que le nom de ce fichier change pour les fonctions de rappel qui diffèrent dans la structure de leurs paramètres. Cet exemple utilise MIDL pour créer le fichier de bibliothèque de types.

3.  Écrivez la fonction de rappel. Les paramètres sont les mêmes que dans l’exemple VBScript de l' [inscription d’un rappel](registering-a-callback.md). Cet exemple imprime une chaîne chaque fois qu’un événement arrive.
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  Ajoutez la fonction de rappel à l’objet [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , comme indiqué dans l’exemple suivant, ou dans un autre objet tel que [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), à l’aide de la bibliothèque de types de rappels appropriée (cbklib. tbl).
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

Dans l’exemple suivant, l’objet [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) est passé à la fonction. La fonction de rappel est ensuite ajoutée en tant que paramètre.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Bibliothèques d’objets utilisées dans l’exemple de code

Les exemples précédents et l’exemple de code de point de contrôle utilisent certaines des bibliothèques d’objets suivantes :

1.  TLBTypes. olb : cette bibliothèque définit certaines des interfaces et types de bibliothèques de types utilisés dans l’exemple de code. Il définit certaines des fonctions à utiliser dans Visual Basic, telles que [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), qui sont déjà disponibles en C ou C++.
2.  VboostTypes6. olb : cette bibliothèque définit certains types de base utilisés dans TLBTypes. olb et FunctionDelegator. bas. Vous trouverez plus d’informations sur TLBTypes dans le livre *Advanced Visual Basic 6 : Power techniques for quotidiens Programs*, par Matthew Curland (Addison-Wesley, juillet 2000, ISBN : 0-201-70712-8). (Ce livre peut ne pas être disponible dans certains langages et pays.)

L’exemple de code du point de contrôle et les bibliothèques suivantes sont associés à cette section et sont nécessaires pour implémenter ce rappel. Ils se trouvent avec l’exemple de code du point de contrôle :

-   Cbklib. idl
-   Cbklib. tlb
-   VboostTypes6. olb
-   TLBTypes. olb
-   FunctionDelegator. bas

 

 
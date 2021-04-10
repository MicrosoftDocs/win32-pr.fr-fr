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
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="5f4e8-103">Inscription d’un rappel dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5f4e8-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="5f4e8-104">L’ajout d’un rappel dans Visual Basic est différent de la méthode utilisée dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="5f4e8-105">La fonction **getRef** utilisée dans VBScript est différente de celle utilisée dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="5f4e8-106">Par conséquent, un développeur doit créer un objet [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui a la fonction de rappel comme méthode par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="5f4e8-107">Cette rubrique fournit les informations nécessaires pour développer des applications Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="5f4e8-108">**Pour implémenter ce rappel dans une application**</span><span class="sxs-lookup"><span data-stu-id="5f4e8-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="5f4e8-109">Ajoutez des références à deux bibliothèques d’objets : TLBTypes. olb et VboostTypes6. olb.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="5f4e8-110">Ces bibliothèques d’objets sont fournies avec l’exemple de code de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="5f4e8-111">Ajoutez une référence à Cbklib. tlb.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="5f4e8-112">Ce fichier définit la structure de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="5f4e8-113">Cbklib. tlb est créé à l’aide du fichier cbklib. idl inclus dans le cadre de l’exemple de code du point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="5f4e8-114">Il est recommandé que le nom de ce fichier change pour les fonctions de rappel qui diffèrent dans la structure de leurs paramètres.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="5f4e8-115">Cet exemple utilise MIDL pour créer le fichier de bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="5f4e8-116">Écrivez la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-116">Write the callback function.</span></span> <span data-ttu-id="5f4e8-117">Les paramètres sont les mêmes que dans l’exemple VBScript de l' [inscription d’un rappel](registering-a-callback.md).</span><span class="sxs-lookup"><span data-stu-id="5f4e8-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="5f4e8-118">Cet exemple imprime une chaîne chaque fois qu’un événement arrive.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-118">This example prints a string whenever an event arrives.</span></span>
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

    

4.  <span data-ttu-id="5f4e8-119">Ajoutez la fonction de rappel à l’objet [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , comme indiqué dans l’exemple suivant, ou dans un autre objet tel que [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), à l’aide de la bibliothèque de types de rappels appropriée (cbklib. tbl).</span><span class="sxs-lookup"><span data-stu-id="5f4e8-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
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

    

<span data-ttu-id="5f4e8-120">Dans l’exemple suivant, l’objet [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) est passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="5f4e8-121">La fonction de rappel est ensuite ajoutée en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="5f4e8-122">Bibliothèques d’objets utilisées dans l’exemple de code</span><span class="sxs-lookup"><span data-stu-id="5f4e8-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="5f4e8-123">Les exemples précédents et l’exemple de code de point de contrôle utilisent certaines des bibliothèques d’objets suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f4e8-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="5f4e8-124">TLBTypes. olb : cette bibliothèque définit certaines des interfaces et types de bibliothèques de types utilisés dans l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="5f4e8-125">Il définit certaines des fonctions à utiliser dans Visual Basic, telles que [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), qui sont déjà disponibles en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="5f4e8-126">VboostTypes6. olb : cette bibliothèque définit certains types de base utilisés dans TLBTypes. olb et FunctionDelegator. bas. Vous trouverez plus d’informations sur TLBTypes dans le livre *Advanced Visual Basic 6 : Power techniques for quotidiens Programs*, par Matthew Curland (Addison-Wesley, juillet 2000, ISBN : 0-201-70712-8).</span><span class="sxs-lookup"><span data-stu-id="5f4e8-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="5f4e8-127">(Ce livre peut ne pas être disponible dans certains langages et pays.)</span><span class="sxs-lookup"><span data-stu-id="5f4e8-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="5f4e8-128">L’exemple de code du point de contrôle et les bibliothèques suivantes sont associés à cette section et sont nécessaires pour implémenter ce rappel.</span><span class="sxs-lookup"><span data-stu-id="5f4e8-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="5f4e8-129">Ils se trouvent avec l’exemple de code du point de contrôle :</span><span class="sxs-lookup"><span data-stu-id="5f4e8-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="5f4e8-130">Cbklib. idl</span><span class="sxs-lookup"><span data-stu-id="5f4e8-130">Cbklib.idl</span></span>
-   <span data-ttu-id="5f4e8-131">Cbklib. tlb</span><span class="sxs-lookup"><span data-stu-id="5f4e8-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="5f4e8-132">VboostTypes6. olb</span><span class="sxs-lookup"><span data-stu-id="5f4e8-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="5f4e8-133">TLBTypes. olb</span><span class="sxs-lookup"><span data-stu-id="5f4e8-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="5f4e8-134">FunctionDelegator. bas</span><span class="sxs-lookup"><span data-stu-id="5f4e8-134">FunctionDelegator.bas</span></span>

 

 
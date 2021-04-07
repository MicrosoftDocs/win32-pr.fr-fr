---
title: Inscription d’un rappel
description: Si l’application requiert une notification lorsque la valeur d’une variable d’état change ou que l’instance de service qu’elle représente devient indisponible, l’application doit inscrire une fonction de rappel.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9095ab4b5b2d43a12f7e806eabc24b174a0311
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728093"
---
# <a name="registering-a-callback"></a><span data-ttu-id="b70b4-103">Inscription d’un rappel</span><span class="sxs-lookup"><span data-stu-id="b70b4-103">Registering a Callback</span></span>

<span data-ttu-id="b70b4-104">Si l’application requiert une notification lorsque la valeur d’une variable d’état change ou que l’instance de service qu’elle représente devient indisponible, l’application doit inscrire une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="b70b4-104">If the application requires notification when the value of a state variable changes or the service instance it represents becomes unavailable, the application must register a callback function.</span></span> <span data-ttu-id="b70b4-105">Pour inscrire une fonction de rappel pour l’objet de service à appeler, utilisez la méthode [**IUPnPService :: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="b70b4-105">To register a callback function for the service object to invoke, use the [**IUPnPService::AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="b70b4-106">Cette méthode peut être utilisée pour inscrire plusieurs rappels.</span><span class="sxs-lookup"><span data-stu-id="b70b4-106">This method can be used to register more than one callback.</span></span>

<span data-ttu-id="b70b4-107">Les développeurs ne doivent pas annuler une opération asynchrone à l’intérieur d’un rappel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b70b4-107">Developers should not cancel an asynchronous operation inside an asynchronous callback.</span></span>

> [!Note]  
> <span data-ttu-id="b70b4-108">L’ajout d’un rappel dans Visual Basic est différent de la méthode utilisée dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="b70b4-108">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="b70b4-109">La fonction **getRef** utilisée dans le VBScript n’est pas disponible dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b70b4-109">The **GetRef** function used in the VBScript is not available in Visual Basic.</span></span> <span data-ttu-id="b70b4-110">Par conséquent, un développeur doit créer un objet [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui a la fonction de rappel comme méthode par défaut.</span><span class="sxs-lookup"><span data-stu-id="b70b4-110">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="b70b4-111">Consultez [inscription d’un rappel dans Visual Basic](registering-a-callback-in-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="b70b4-111">See [Registering a Callback in Visual Basic](registering-a-callback-in-visual-basic.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="b70b4-112">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="b70b4-112">VBScript Example</span></span>

<span data-ttu-id="b70b4-113">Le code VBScript suivant définit la fonction de rappel **serviceChangeCallback**, à appeler lorsque les valeurs des variables d’État changent ou lorsque l’instance de service devient indisponible.</span><span class="sxs-lookup"><span data-stu-id="b70b4-113">The following VBScript code defines the callback function **serviceChangeCallback**, to be invoked when the values of state variables change or when the service instance becomes unavailable.</span></span> <span data-ttu-id="b70b4-114">La fonction a quatre arguments.</span><span class="sxs-lookup"><span data-stu-id="b70b4-114">The function has four arguments.</span></span>

<span data-ttu-id="b70b4-115">Le premier argument de la fonction spécifie la raison pour laquelle le rappel est appelé.</span><span class="sxs-lookup"><span data-stu-id="b70b4-115">The first argument to the function specifies the reason the callback is invoked.</span></span> <span data-ttu-id="b70b4-116">Elle est appelée soit parce qu’une variable d’État a changé, soit parce que l’instance de service est devenue indisponible.</span><span class="sxs-lookup"><span data-stu-id="b70b4-116">It is invoked either because a state variable changed, or because the service instance has become unavailable.</span></span>

<span data-ttu-id="b70b4-117">Le deuxième argument est l’objet de service pour lequel le rappel est appelé.</span><span class="sxs-lookup"><span data-stu-id="b70b4-117">The second argument is the Service object for which the callback is invoked.</span></span> <span data-ttu-id="b70b4-118">Si le rappel est appelé pour une modification de variable d’État, deux arguments supplémentaires sont passés à la fonction : le nom de la variable qui a changé et sa nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="b70b4-118">If the callback is invoked for a state variable change, then the function is passed two additional arguments: the name of the variable that changed, and its new value.</span></span>

<span data-ttu-id="b70b4-119">Dans cet exemple, le rappel affiche simplement une boîte de message qui indique le nom de la variable modifiée et sa nouvelle valeur, et si le rappel a été appelé pour une modification de variable d’État.</span><span class="sxs-lookup"><span data-stu-id="b70b4-119">In this example, the callback simply displays a message box that shows the name of the changed variable and its new value, and if the callback was invoked for a state variable change.</span></span> <span data-ttu-id="b70b4-120">Dans le cas contraire, il affiche un message indiquant que l’instance de service n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="b70b4-120">Otherwise, it displays a message that indicates the service instance is no longer available.</span></span>

<span data-ttu-id="b70b4-121">La dernière partie du fragment de code montre comment inscrire la fonction de rappel à l’aide de la méthode [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) .</span><span class="sxs-lookup"><span data-stu-id="b70b4-121">The last part of the code fragment shows how to register the callback function using the [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) method.</span></span> <span data-ttu-id="b70b4-122">Les variables d’objet de service, *appService* et *xportService* , sont supposées avoir été initialisées comme indiqué dans [obtention d’objets de service](obtaining-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b70b4-122">The service object variables, *appService* and *xportService* are assumed to have been initialized as shown in [Obtaining Service Objects](obtaining-service-objects.md).</span></span>


```VB
'State Change Callback Function
 
'Note:  In the sub declaration statement below, VARIABLE_UPDATE
'is one of two possible values for the callbackType argument; 
'the other is SERVICE_INSTANCE_DIED

Sub serviceChangeCallback(callbacktype, svcObj, varName, value)
    If (callbacktype = "VARIABLE_UPDATE") then
        Dim outString
        outString = "State Variable Changed:" & vbCrLf
        outString = outString & varName & " == " & value
    
        MsgBox(outString, "Service Callback")
    Else if (callbacktype = "SERVICE_INSTANCE_DIED") then
        MsgBox("Service instance is no longer available", 
               "Service Callback")
    End If
End Sub

' ...
    
'Add our state change callback to each service
appService.AddCallback GetRef("serviceChangeCallback")
xportService.AddCallback GetRef("serviceChangeCallback")
```



## <a name="c-example"></a><span data-ttu-id="b70b4-123">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="b70b4-123">C++ Example</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

class CUPnPServiceCallback : public IUPnPServiceCallback
{
public:
    CUPnPServiceCallback()
    {
        m_lRefCount = 0;
    };
    
    STDMETHODIMP QueryInterface(REFIID iid, LPVOID* ppvObject)
    {
        HRESULT hr = S_OK;
        
        if(NULL == ppvObject)
        {
            hr = E_POINTER;
        }
        else
        {
            *ppvObject = NULL;
        }
        
        if(SUCCEEDED(hr))
        {
            if(IsEqualIID(iid, IID_IUnknown) || IsEqualIID(iid, IID_IUPnPServiceCallback))
            {
                *ppvObject = static_cast<IUPnPServiceCallback*>(this);
                AddRef();
            }
            else
            {
                hr = E_NOINTERFACE;
            }
        }
        
        return hr;
    };
    
    STDMETHODIMP_(ULONG) AddRef()
    {
        return ::InterlockedIncrement(&m_lRefCount);
    };
    
    STDMETHODIMP_(ULONG) Release()
    {
        LONG lRefCount = ::InterlockedDecrement(&m_lRefCount);
        if(0 == lRefCount)
        {
            delete this;
        }
        
        return lRefCount;
    };
    
    STDMETHODIMP StateVariableChanged(IUPnPService *pus, LPCWSTR pcwszStateVarName, VARIANT varValue)
    {
        HRESULT    hr = S_OK;
        BSTR ServiceId;
        hr = pus->get_Id(&ServiceId);
        if (SUCCEEDED(hr))
        {
            VARIANT AlphaVariant;
            VariantInit(&AlphaVariant);
            hr = VariantChangeType(&AlphaVariant, &varValue, VARIANT_ALPHABOOL, VT_BSTR);
            if(SUCCEEDED(hr))
            {
                printf("StateVariableChanged called for the %S service"
                       " for %S state variable with the value=%S.\n",
                        ServiceId, pcwszStateVarName, V_BSTR(&AlphaVariant));
                VariantClear(&AlphaVariant);
            }
            SysFreeString(ServiceId);
        }
        return hr;
    };

    STDMETHODIMP ServiceInstanceDied(IUPnPService *pus)
    {
        HRESULT hr = S_OK;
        BSTR ServiceType;
        hr = pus->get_ServiceTypeIdentifier(&ServiceType);
        if(SUCCEEDED(hr))
        {
            printf("ServiceInstanceDied called for the %S service!\n", ServiceType);
            SysFreeString(ServiceType);
        }
        return hr;
    };
    
private:
    LONG m_lRefCount;
    
};

HRESULT AddCallbackToService(IUPnPService* pUPnPService)
{
    HRESULT hr = S_OK;

    IUnknown* pUPnPServiceCallback = new CUPnPServiceCallback;
    if(NULL != pUPnPServiceCallback)
    {
        pUPnPServiceCallback->AddRef();
        hr = pUPnPService->AddCallback(pUPnPServiceCallback);
        pUPnPServiceCallback->Release();
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
    return hr;
}
```



 

 
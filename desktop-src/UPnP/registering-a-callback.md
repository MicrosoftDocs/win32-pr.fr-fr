---
title: Inscription d’un rappel
description: Si l’application requiert une notification lorsque la valeur d’une variable d’état change ou que l’instance de service qu’elle représente devient indisponible, l’application doit inscrire une fonction de rappel.
ms.assetid: 881e71f7-39e6-4847-bdf2-78e54d1750cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3dca603e6226d3171aed920311bafcf6844ec9fab5c7aa05deafee7a13fd8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768529"
---
# <a name="registering-a-callback"></a>Inscription d’un rappel

Si l’application requiert une notification lorsque la valeur d’une variable d’état change ou que l’instance de service qu’elle représente devient indisponible, l’application doit inscrire une fonction de rappel. Pour inscrire une fonction de rappel pour l’objet de service à appeler, utilisez la méthode [**IUPnPService :: AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Cette méthode peut être utilisée pour inscrire plusieurs rappels.

Les développeurs ne doivent pas annuler une opération asynchrone à l’intérieur d’un rappel asynchrone.

> [!Note]  
> l’ajout d’un rappel dans Visual Basic est différent de la méthode utilisée dans VBScript. La fonction **getRef** utilisée dans le VBScript n’est pas disponible dans Visual Basic. Par conséquent, un développeur doit créer un objet [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui a la fonction de rappel comme méthode par défaut. Consultez [inscription d’un rappel dans Visual Basic](registering-a-callback-in-visual-basic.md).

 

## <a name="vbscript-example"></a>Exemple VBScript

Le code VBScript suivant définit la fonction de rappel **serviceChangeCallback**, à appeler lorsque les valeurs des variables d’État changent ou lorsque l’instance de service devient indisponible. La fonction a quatre arguments.

Le premier argument de la fonction spécifie la raison pour laquelle le rappel est appelé. Elle est appelée soit parce qu’une variable d’État a changé, soit parce que l’instance de service est devenue indisponible.

Le deuxième argument est l’objet de service pour lequel le rappel est appelé. Si le rappel est appelé pour une modification de variable d’État, deux arguments supplémentaires sont passés à la fonction : le nom de la variable qui a changé et sa nouvelle valeur.

Dans cet exemple, le rappel affiche simplement une boîte de message qui indique le nom de la variable modifiée et sa nouvelle valeur, et si le rappel a été appelé pour une modification de variable d’État. Dans le cas contraire, il affiche un message indiquant que l’instance de service n’est plus disponible.

La dernière partie du fragment de code montre comment inscrire la fonction de rappel à l’aide de la méthode [**AddCallback**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-addcallback) . Les variables d’objet de service, *appService* et *xportService* , sont supposées avoir été initialisées comme indiqué dans [obtention d’objets de service](obtaining-service-objects.md).


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



## <a name="c-example"></a>Exemple C++


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



 

 
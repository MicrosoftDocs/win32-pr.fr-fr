---
title: Appel d’actions
description: La méthode IUPnPService InvokeAction permet d’appeler des actions sur des objets de service.
ms.assetid: 671e9280-5ead-43f2-bb6b-12792a6a4487
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7550575281681f3f533db90ef1c1034dbaa085
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382399"
---
# <a name="invoking-actions"></a>Appel d’actions

La méthode [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permet d’appeler des actions sur des objets de service. Cette méthode a deux paramètres d’entrée : le nom d’une action et un tableau d’arguments d’entrée pour cette action. La méthode a deux paramètres :

-   Paramètre un : paramètre d’entrée/sortie : un tableau d’arguments de sortie pour cette action.
-   Le deuxième paramètre, un paramètre de sortie : une valeur de retour.

La méthode provoque l’appel de l’action sur l’appareil. L’appareil génère des notifications d’événements si l’action entraîne la modification des variables d’état de l’appareil.

## <a name="vbscript-example"></a>Exemple VBScript

L’exemple de code VBScript suivant appelle deux actions sur un objet de service. La première action, *GetTrackInfo*, accepte un argument d’entrée, un numéro de piste. L’action *GetTrackInfo* retourne la longueur de la piste comme valeur de retour. L’action a également un argument de sortie, qui contient le titre de piste si la méthode retourne une réussite.

Après l’appel de l’action *GetTrackInfo* , l’exemple appelle l’action Play, qui n’accepte aucun argument. Toutefois, étant donné que la syntaxe de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiert un tableau d’arguments d’entrée et de sortie, l’exemple doit créer un tableau vide, *emptyArgs*, sans éléments. L’exemple passe ce tableau à **InvokeAction** pour les arguments d’entrée et de sortie, ainsi que le nom de l’action.


```VB
Dim returnVal
Dim outArgs(1)
Dim args(1)
args(0) = 3
returnVal = service.InvokeAction("GetTrackInfo", args, outArgs)
'return Val now contains the track length
'and outArgs(0) contains the track title
Dim emptyArgs(0)
returnVal = service.InvokeAction("Play", emptyArgs, emptyArgs)
'returnVal indicates if the action was successful
```



## <a name="c-example"></a>Exemple C++

L’exemple suivant définit une fonction C++ qui appelle une action sans argument. Étant donné que [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiert un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) d’arguments à passer, cet exemple crée un **SAFEARRAY** vide. Étant donné que cette action ne retourne pas de valeur ou a des arguments de sortie, cet exemple ignore les deux dernières valeurs [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passées à **InvokeAction**.

L’appareil génère des notifications d’événements si l’action entraîne la modification des variables d’état de l’appareil.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokePlay(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"Play");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 0;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            LONG    lStatus;
            VARIANT varInArgs;

            VariantInit(&varInArgs);

            varInArgs.vt = VT_VARIANT | VT_ARRAY;

            V_ARRAY(&varInArgs) = psa;

            hr = pService->InvokeAction(bstrActionName,
                                        varInArgs,
                                        NULL,
                                        NULL);

            if (SUCCEEDED(hr))
            {
                wcout << L"Action invoked successfully\n"; 
            }
            else
            {
                wcerr << L"Failed to invoke action - HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        

            }                                   

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



L’exemple suivant appelle l’action *GetTrackInfo* fictive. Elle prend un numéro de piste comme argument, retourne la longueur de la piste comme valeur de retour et retourne le titre de piste dans un argument de sortie. Le code est similaire à l’exemple précédent, sauf qu’au lieu de créer un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vide d’arguments d’entrée, cet exemple insère un [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) qui contient le numéro de piste. Si [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) retourne Success, cet exemple examine la valeur de retour et le tableau d’arguments de sortie.


```C++
#include <windows.h>
#include <upnp.h>
#include <iostream>
#include <iomanip>

#pragma comment(lib, "oleaut32.lib")

using namespace std;

void InvokeGetTrackInfo(IUPnPService * pService)
{
    HRESULT hr;
    BSTR bstrActionName;

    bstrActionName = SysAllocString(L"GetTrackInfo");

    if (bstrActionName)
    {
        SAFEARRAYBOUND  rgsaBound[1];
        SAFEARRAY       * psa = NULL;

        rgsaBound[0].lLbound = 0;
        rgsaBound[0].cElements = 1;

        psa = SafeArrayCreate(VT_VARIANT, 1, rgsaBound);

        if (psa)
        {
            long rgIndices[1];
            VARIANT varTrackNum;

            rgIndices[0] = 0;
            VariantInit(&varTrackNum);

            varTrackNum.vt = VT_I4;
            // An arbitrary track is chosen (track 3)
            V_I4(&varTrackNum) = 3;

            hr = SafeArrayPutElement(psa,
                                     rgIndices,
                                     (void *) &varTrackNum);

            VariantClear(&varTrackNum);

            if (SUCCEEDED(hr))
            {            
                LONG    lStatus;
                VARIANT varInArgs;
                VARIANT varOutArgs;
                VARIANT varReturnVal;

                VariantInit(&varInArgs);
                VariantInit(&varOutArgs);
                VariantInit(&varReturnVal);

                varInArgs.vt = VT_VARIANT | VT_ARRAY;

                V_ARRAY(&varInArgs) = psa;

                hr = pService->InvokeAction(bstrActionName,
                                            varInArgs,
                                            &varOutArgs,
                                            &varReturnVal);

                if (SUCCEEDED(hr))
                {
                    SAFEARRAY * psaOutArgs = NULL;
                    VARIANT   varTrackTitle;

                    psaOutArgs = V_ARRAY(&varOutArgs);
                    VariantInit(&varTrackTitle);

                    rgIndices[0] = 0;
                    hr = SafeArrayGetElement(psaOutArgs,
                                             rgIndices,
                                             (void *)&varTrackTitle);                    

                    if (SUCCEEDED(hr))
                    {                    
                        wcout << L"Action invoked successfully\n"
                              << L"\tTrack Length == " 
                              << V_I4(&varReturnVal) << L"\n"
                              << L"\tTrack Title == " 
                              << V_BSTR(&varTrackTitle) << L"\n";
                    }
                    else
                    {
                        wcerr << L"Failed to get array element -"
                              << L" HRESULT 0x" 
                              << setbase(16)
                              << hr << L"\n";                        
                    }

                    VariantClear(&varTrackTitle);
                    VariantClear(&varReturnVal);
                    VariantClear(&varOutArgs);
                }
                else
                {
                    wcerr << L"Failed to invoke action - HRESULT 0x" 
                          << setbase(16)
                          << hr << L"\n";                        
                }                                   
            }
            else
            {
                wcerr << L"Failed to insert argument into array - "
                      << L"HRESULT 0x" 
                      << setbase(16)
                      << hr << L"\n";                        
            }

            SafeArrayDestroy(psa);
        }
        else
        {
            wcerr << L"Failed to create safe array\n";
        }   

        SysFreeString(bstrActionName);
    }
    else
    {
        wcerr << L"Failed to allocate action name string\n";
    }
}
```



 

 
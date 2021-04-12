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
# <a name="invoking-actions"></a><span data-ttu-id="db41b-103">Appel d’actions</span><span class="sxs-lookup"><span data-stu-id="db41b-103">Invoking Actions</span></span>

<span data-ttu-id="db41b-104">La méthode [**IUPnPService :: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) permet d’appeler des actions sur des objets de service.</span><span class="sxs-lookup"><span data-stu-id="db41b-104">The [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) method allows actions to be invoked on Service objects.</span></span> <span data-ttu-id="db41b-105">Cette méthode a deux paramètres d’entrée : le nom d’une action et un tableau d’arguments d’entrée pour cette action.</span><span class="sxs-lookup"><span data-stu-id="db41b-105">This method has two input parameters: the name of an action and an array of input arguments to that action.</span></span> <span data-ttu-id="db41b-106">La méthode a deux paramètres :</span><span class="sxs-lookup"><span data-stu-id="db41b-106">The method has two parameters:</span></span>

-   <span data-ttu-id="db41b-107">Paramètre un : paramètre d’entrée/sortie : un tableau d’arguments de sortie pour cette action.</span><span class="sxs-lookup"><span data-stu-id="db41b-107">Parameter one — an input/output parameter: an array of output arguments for that action.</span></span>
-   <span data-ttu-id="db41b-108">Le deuxième paramètre, un paramètre de sortie : une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="db41b-108">Parameter two — an output parameter: a return value.</span></span>

<span data-ttu-id="db41b-109">La méthode provoque l’appel de l’action sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="db41b-109">The method causes the action to be invoked on the device.</span></span> <span data-ttu-id="db41b-110">L’appareil génère des notifications d’événements si l’action entraîne la modification des variables d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="db41b-110">The device generates event notifications if the action causes state variables of the device to change.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="db41b-111">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="db41b-111">VBScript Example</span></span>

<span data-ttu-id="db41b-112">L’exemple de code VBScript suivant appelle deux actions sur un objet de service.</span><span class="sxs-lookup"><span data-stu-id="db41b-112">The following VBScript code example invokes two actions on a Service object.</span></span> <span data-ttu-id="db41b-113">La première action, *GetTrackInfo*, accepte un argument d’entrée, un numéro de piste.</span><span class="sxs-lookup"><span data-stu-id="db41b-113">The first action, *GetTrackInfo*, takes one input argument, a track number.</span></span> <span data-ttu-id="db41b-114">L’action *GetTrackInfo* retourne la longueur de la piste comme valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="db41b-114">The *GetTrackInfo* action returns the track length as the return value.</span></span> <span data-ttu-id="db41b-115">L’action a également un argument de sortie, qui contient le titre de piste si la méthode retourne une réussite.</span><span class="sxs-lookup"><span data-stu-id="db41b-115">The action also has one output argument, which contains the track title if the method returns success.</span></span>

<span data-ttu-id="db41b-116">Après l’appel de l’action *GetTrackInfo* , l’exemple appelle l’action Play, qui n’accepte aucun argument.</span><span class="sxs-lookup"><span data-stu-id="db41b-116">After invoking the *GetTrackInfo* action, the example invokes the Play action, which takes no arguments.</span></span> <span data-ttu-id="db41b-117">Toutefois, étant donné que la syntaxe de [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiert un tableau d’arguments d’entrée et de sortie, l’exemple doit créer un tableau vide, *emptyArgs*, sans éléments.</span><span class="sxs-lookup"><span data-stu-id="db41b-117">However, because the syntax of [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires an array of both input and output arguments, the example must create an empty array, *emptyArgs*, with no elements.</span></span> <span data-ttu-id="db41b-118">L’exemple passe ce tableau à **InvokeAction** pour les arguments d’entrée et de sortie, ainsi que le nom de l’action.</span><span class="sxs-lookup"><span data-stu-id="db41b-118">The example passes this array to **InvokeAction** for both the input and output arguments, along with the name of the action.</span></span>


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



## <a name="c-example"></a><span data-ttu-id="db41b-119">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="db41b-119">C++ Example</span></span>

<span data-ttu-id="db41b-120">L’exemple suivant définit une fonction C++ qui appelle une action sans argument.</span><span class="sxs-lookup"><span data-stu-id="db41b-120">The following example defines a C++ function that invokes an action with no arguments.</span></span> <span data-ttu-id="db41b-121">Étant donné que [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requiert un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) d’arguments à passer, cet exemple crée un **SAFEARRAY** vide.</span><span class="sxs-lookup"><span data-stu-id="db41b-121">Because [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) requires a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of arguments to be passed in, this example creates an empty **SAFEARRAY**.</span></span> <span data-ttu-id="db41b-122">Étant donné que cette action ne retourne pas de valeur ou a des arguments de sortie, cet exemple ignore les deux dernières valeurs [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) passées à **InvokeAction**.</span><span class="sxs-lookup"><span data-stu-id="db41b-122">Since this action does not return a value or have output arguments, this example ignores the last two [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) values passed to **InvokeAction**.</span></span>

<span data-ttu-id="db41b-123">L’appareil génère des notifications d’événements si l’action entraîne la modification des variables d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="db41b-123">The device generates event notifications if the action causes state variables of the device to change.</span></span>


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



<span data-ttu-id="db41b-124">L’exemple suivant appelle l’action *GetTrackInfo* fictive.</span><span class="sxs-lookup"><span data-stu-id="db41b-124">The following example invokes the fictitious *GetTrackInfo* action.</span></span> <span data-ttu-id="db41b-125">Elle prend un numéro de piste comme argument, retourne la longueur de la piste comme valeur de retour et retourne le titre de piste dans un argument de sortie.</span><span class="sxs-lookup"><span data-stu-id="db41b-125">It takes a track number as an argument, returns the track length as a return value, and returns the track title in an output argument.</span></span> <span data-ttu-id="db41b-126">Le code est similaire à l’exemple précédent, sauf qu’au lieu de créer un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) vide d’arguments d’entrée, cet exemple insère un [**Variant**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) qui contient le numéro de piste.</span><span class="sxs-lookup"><span data-stu-id="db41b-126">The code is similar to the previous example, except that instead of creating an empty [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of input arguments, this example inserts a [**VARIANT**](/previous-versions/windows/desktop/automat/variant-manipulation-functions) that contains the track number.</span></span> <span data-ttu-id="db41b-127">Si [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) retourne Success, cet exemple examine la valeur de retour et le tableau d’arguments de sortie.</span><span class="sxs-lookup"><span data-stu-id="db41b-127">If [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) returns success, this example examines the return value and the array of output arguments.</span></span>


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



 

 
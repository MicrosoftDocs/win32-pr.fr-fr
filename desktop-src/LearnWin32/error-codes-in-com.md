---
title: Codes d’erreur dans COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725388"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="6cbb2-103">Codes d’erreur dans COM</span><span class="sxs-lookup"><span data-stu-id="6cbb2-103">Error Codes in COM</span></span>

<span data-ttu-id="6cbb2-104">Pour indiquer la réussite ou l’échec, les méthodes et les fonctions COM retournent une valeur de type **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="6cbb2-105">Un **HRESULT** est un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="6cbb2-106">Le bit de poids fort de la valeur **HRESULT** signale la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="6cbb2-107">Zéro (0) indique une réussite et 1 indique un échec.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="6cbb2-108">Cela produit les plages numériques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cbb2-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="6cbb2-109">Codes de réussite : 0x0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="6cbb2-110">Codes d’erreur : 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="6cbb2-111">Un petit nombre de méthodes COM ne retournent pas de valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cbb2-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="6cbb2-112">Par exemple, les méthodes [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) retournent des valeurs long non signées.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="6cbb2-113">Toutefois, chaque méthode COM qui retourne un code d’erreur en retournant une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cbb2-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="6cbb2-114">Pour vérifier si une méthode COM est réussie, examinez le bit de poids fort de la valeur **HRESULT** retournée.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="6cbb2-115">Les en-têtes SDK Windows fournissent deux macros qui facilitent cette opération : la macro [**Succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) et la macro qui [**a échoué**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="6cbb2-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="6cbb2-116">La macro **Succeeded** retourne la **valeur true** si un **HRESULT** est un code de réussite et **false** s’il s’agit d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="6cbb2-117">L’exemple suivant vérifie si [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) est correctement effectué.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="6cbb2-118">Il est parfois plus pratique de tester la condition inverse.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="6cbb2-119">La macro [**ayant échoué**](/windows/desktop/api/winerror/nf-winerror-failed) fait l’inverse de la [**réussite**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span><span class="sxs-lookup"><span data-stu-id="6cbb2-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="6cbb2-120">Elle retourne **true** pour un code d’erreur et **false** pour un code de réussite.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="6cbb2-121">Plus loin dans ce module, nous examinerons quelques conseils pratiques sur la façon de structurer votre code pour gérer les erreurs COM.</span><span class="sxs-lookup"><span data-stu-id="6cbb2-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="6cbb2-122">(Voir [gestion des erreurs dans com](error-handling-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="6cbb2-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="6cbb2-123">Suivant</span><span class="sxs-lookup"><span data-stu-id="6cbb2-123">Next</span></span>

[<span data-ttu-id="6cbb2-124">Création d’un objet dans COM</span><span class="sxs-lookup"><span data-stu-id="6cbb2-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
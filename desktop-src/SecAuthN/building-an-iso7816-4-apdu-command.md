---
description: La procédure suivante donne un bref aperçu du processus de génération.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Génération d’une commande APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201830"
---
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="fa50f-103">Génération d’une commande APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="fa50f-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="fa50f-104">Pour ajouter des fonctionnalités à un fournisseur de services, vous devez savoir comment une unité de [*données de protocole d’application*](/windows/desktop/SecGloss/a-gly) (APDU) ISO7816-4 est générée dans les dll du fournisseur de services de base.</span><span class="sxs-lookup"><span data-stu-id="fa50f-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="fa50f-105">La procédure suivante donne un bref aperçu du processus de génération.</span><span class="sxs-lookup"><span data-stu-id="fa50f-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="fa50f-106">L’exemple inclus ici n’est pas nécessairement complet. Pour plus d’informations, consultez les exemples d’applications et de dll.</span><span class="sxs-lookup"><span data-stu-id="fa50f-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="fa50f-107">**Pour générer une commande APDU ISO7816-4**</span><span class="sxs-lookup"><span data-stu-id="fa50f-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="fa50f-108">Créez un objet [**ISCardCmd**](iscardcmd.md) et un objet [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="fa50f-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    <span data-ttu-id="fa50f-109">L’interface [**ISCardCmd**](iscardcmd.md) contient deux mémoires tampons **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="fa50f-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="fa50f-110">Une mémoire tampon contient la chaîne de commande APDU réelle (plus toutes les données à envoyer avec la commande).</span><span class="sxs-lookup"><span data-stu-id="fa50f-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="fa50f-111">L’autre contient toutes les informations de réponse retournées par la carte après l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="fa50f-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="fa50f-112">À l’aide de ces objets, créez une commande ISO7816-4 valide comme suit :</span><span class="sxs-lookup"><span data-stu-id="fa50f-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="fa50f-113">Voici le code utilisé dans la méthode [**GetChallenge**](iscardiso7816-getchallenge.md) :</span><span class="sxs-lookup"><span data-stu-id="fa50f-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    <span data-ttu-id="fa50f-114">La méthode [**ISCardISO7816 :: GetChallenge**](iscardiso7816-getchallenge.md) utilise la méthode [**ISCardCmd :: BuildCmd**](iscardcmd-buildcmd.md) pour générer l’APDU demandée.</span><span class="sxs-lookup"><span data-stu-id="fa50f-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="fa50f-115">Pour ce faire, vous écrivez les informations appropriées dans le tampon [**ISCardCmd**](iscardcmd.md) APDU dans l’instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="fa50f-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="fa50f-116">À l’aide de l’objet [**ISCardCmd**](iscardcmd.md) généré, effectuez une transaction avec la carte, interprétez les résultats et continuez.</span><span class="sxs-lookup"><span data-stu-id="fa50f-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="fa50f-117">Développement au-delà de ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="fa50f-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="fa50f-118">La méthode recommandée pour développer le processus de génération et d’exécution du fournisseur de services décrite ci-dessus consiste à créer un nouvel objet COM.</span><span class="sxs-lookup"><span data-stu-id="fa50f-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="fa50f-119">Cet objet COM doit prendre en charge une nouvelle interface qui autorise la création de commandes non-ISO7816-4 et qui doit agréger l’interface [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="fa50f-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="fa50f-120">Exemple de création d’une commande APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="fa50f-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="fa50f-121">L’exemple suivant montre le code utilisé dans la procédure ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="fa50f-121">The following example shows the code used in the procedure above.</span></span>


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 

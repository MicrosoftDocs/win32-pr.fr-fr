---
title: Interprétation des informations de liaison
description: Microsoft RPC permet à vos programmes client et serveur d’accéder aux informations contenues dans un handle de liaison et de les interpréter.
ms.assetid: 0116b7a1-85f8-4860-8fba-4aa1960c6799
keywords:
- Appel de procédure distante RPC, tâches, interprétation de la liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423564a844bfbf959de8a2fcf4dfff5ae86b8b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462454"
---
# <a name="interpreting-binding-information"></a><span data-ttu-id="e3d8e-104">Interprétation des informations de liaison</span><span class="sxs-lookup"><span data-stu-id="e3d8e-104">Interpreting Binding Information</span></span>

<span data-ttu-id="e3d8e-105">Microsoft RPC permet à vos programmes client et serveur d’accéder aux informations contenues dans un handle de liaison et de les interpréter.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-105">Microsoft RPC enables your client and server programs access to and interpret the information in a binding handle.</span></span> <span data-ttu-id="e3d8e-106">Cela ne signifie pas que vous pouvez ou devez essayer d’accéder directement au contenu d’un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-106">This does not mean that you can or should try to access the contents of a binding handle directly.</span></span> <span data-ttu-id="e3d8e-107">Microsoft RPC fournit des fonctions qui définissent et récupèrent les informations dans des handles de liaison.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-107">Microsoft RPC provides functions that set and retrieve the information in binding handles.</span></span>

<span data-ttu-id="e3d8e-108">Pour obtenir les informations dans un handle de liaison, transmettez le handle à [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="e3d8e-108">To get the information in a binding handle, pass the handle to [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="e3d8e-109">Elle retourne les informations de liaison sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-109">It returns the binding information as a string.</span></span> <span data-ttu-id="e3d8e-110">Pour chaque appel à **RpcBindingToStringBinding**, vous devez avoir un appel correspondant à la fonction [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span><span class="sxs-lookup"><span data-stu-id="e3d8e-110">For every call to **RpcBindingToStringBinding**, you must have a corresponding call to the function [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree).</span></span>

<span data-ttu-id="e3d8e-111">Vous pouvez appeler la fonction [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) pour analyser la chaîne que vous obtenez à partir de [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span><span class="sxs-lookup"><span data-stu-id="e3d8e-111">You can call the function [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to parse the string you obtain from [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).</span></span> <span data-ttu-id="e3d8e-112">Cette fonction alloue des chaînes pour contenir les informations qu’elle analyse.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-112">This function allocates strings to contain the information it parses.</span></span> <span data-ttu-id="e3d8e-113">Si vous ne souhaitez pas qu’il analyse une partie particulière des informations de liaison, transmettez une valeur **null** comme valeur de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-113">If you do not want it to parse a particular piece of binding information, pass a **NULL** as the value of that parameter.</span></span> <span data-ttu-id="e3d8e-114">Veillez à appeler [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) pour chacune des chaînes qu’il alloue.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-114">Be sure to call [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) for each of the strings it allocates.</span></span>

<span data-ttu-id="e3d8e-115">Le fragment de code suivant illustre comment une application peut appeler ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-115">The following code fragment illustrates how an application might call these functions.</span></span>


```C++
RPC_STATUS status;
UCHAR *lpzStringBinding;
UCHAR *lpzProtocolSequence;
UCHAR *lpzNetworkAddress;
UCHAR *lpzEndpoint;
UCHAR *NetworkOptions;
 
// The variable hBindingHandle is a valid binding handle.
 
status = RpcBindingToStringBinding(hBindingHandle,&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringBindingParse(
    lpzStringBinding,
    NULL,
    &lpzProtocolSequence;
    &lpzNetworkAddress;
    &lpzEndpoint;
    &NetworkOptions);
// Code to check the status goes here.
 
// Code to analyze and alter the binding information in the strings
// goes here.
 
status = RpcStringFree(&lpzStringBinding);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzProtocolSequence);
// Code to check the status goes here.
 
status = RpcStringFree(&lpzNetworkAddress);
// Code to check the status goes here.
 
status = RpcStringFree(&NetworkOptions);
// Code to check the status goes here.
```



<span data-ttu-id="e3d8e-116">L’exemple de code précédent appelle les fonctions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) et [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) pour obtenir et analyser les informations dans un handle de liaison valide.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-116">The preceding sample code calls the functions [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) and [**RpcStringBindingParse**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingparse) to get and parse the information in a valid binding handle.</span></span> <span data-ttu-id="e3d8e-117">Notez que la valeur **null** a été transmise en tant que deuxième paramètre à **RpcStringBindingParse**.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-117">Note that the value **NULL** was passed as the second parameter to **RpcStringBindingParse**.</span></span> <span data-ttu-id="e3d8e-118">Cela provoque l’ignorance de l’analyse de l’UUID de l’objet par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-118">This causes that function to skip parsing the object UUID.</span></span> <span data-ttu-id="e3d8e-119">Étant donné qu’elle n’analyse pas l’UUID, **RpcStringBindingParse** n’alloue pas de chaîne pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-119">Since it does not parse the UUID, **RpcStringBindingParse** will not allocate a string for it.</span></span> <span data-ttu-id="e3d8e-120">Cette technique permet à votre application d’allouer uniquement de la mémoire pour les informations qui vous intéressent à l’analyse et à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="e3d8e-120">This technique enables your application to only allocate memory for the information you are interested in parsing and analyzing.</span></span>

 

 





---
title: C-définitions de compilateur pour les proxys/stubs
description: Le fichier d’en-tête rpcproxy. h comprend les définitions de macro suivantes, qui peuvent être utiles lors de la création d’une application COM distribuée. Ces macros sont appelées avec le commutateur de préprocesseur/D (ou-D) au moment de la compilation C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- Compilateur MIDL MIDL, compilateur C, définitions pour les proxys/stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029606"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="083ca-105">C-définitions de compilateur pour les proxys/stubs</span><span class="sxs-lookup"><span data-stu-id="083ca-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="083ca-106">Le fichier d’en-tête rpcproxy. h comprend les définitions de macro suivantes, qui peuvent être utiles lors de la création d’une application COM distribuée.</span><span class="sxs-lookup"><span data-stu-id="083ca-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="083ca-107">Ces macros sont appelées avec le commutateur de préprocesseur [**/d**](-d.md) (ou-D) au moment de la compilation C.</span><span class="sxs-lookup"><span data-stu-id="083ca-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="083ca-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="083ca-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="083ca-109">Description</span><span class="sxs-lookup"><span data-stu-id="083ca-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="083ca-110">INSCRIRE \_ la \_ dll proxy</span><span class="sxs-lookup"><span data-stu-id="083ca-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="083ca-111">Génère des fonctions **DllMain**, **DllRegisterServer** et **DllUnregisterServer** pour l’inscription automatique d’une dll proxy.</span><span class="sxs-lookup"><span data-stu-id="083ca-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="083ca-112">CLSID du PROXY \_ =<clsid></span><span class="sxs-lookup"><span data-stu-id="083ca-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="083ca-113">Spécifie un identificateur de classe pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="083ca-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="083ca-114">Si cette macro n’est pas définie, le CLSID par défaut est le premier identificateur d’interface que le compilateur MIDL rencontre dans la spécification IDL pour le serveur proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="083ca-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="083ca-115">Le \_ CLSID du proxy \_ est = {0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}}</span><span class="sxs-lookup"><span data-stu-id="083ca-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="083ca-116">Spécifie la valeur de l’identificateur de classe du serveur au format hexadécimal binaire.</span><span class="sxs-lookup"><span data-stu-id="083ca-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="083ca-117">En définissant la macro **\_ \_ dll du proxy d’inscription** lors de la compilation de dlldata. c, votre dll de marshaling de proxy/stub inclut automatiquement les définitions par défaut des fonctions **DllMain**, **DllRegisterServer** et **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="083ca-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="083ca-118">Vous pouvez utiliser ces fonctions pour enregistrer automatiquement votre DLL de proxy dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="083ca-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="083ca-119">Ce code d’inscription par défaut utilise le GUID de la première interface rencontrée comme CLSID pour l’inscription de l’intégralité du serveur DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="083ca-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="083ca-120">Par la suite, COM utilise ce CLSID pour localiser et charger le serveur proxy/stub compilé pour le marshaling des interfaces que le serveur est inscrit pour gérer.</span><span class="sxs-lookup"><span data-stu-id="083ca-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="083ca-121">Lorsqu’une application effectue un appel de méthode d’interface qui franchit les limites du thread, du processus ou de l’ordinateur, COM utilise l’entrée du registre de l’identificateur d’interface pour localiser l’entrée de Registre CLSID pour le serveur de marshaling proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="083ca-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="083ca-122">Il utilise ensuite ce CLSID pour charger le serveur (s’il n’est pas déjà chargé) afin que l’appel d’interface puisse être marshalé.</span><span class="sxs-lookup"><span data-stu-id="083ca-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="083ca-123">Utilisez la macro **proxy \_ CLSID** = <clsid> lorsque vous souhaitez spécifier explicitement le CLSID du serveur proxy/stub au lieu de s’appuyer sur le CLSID par défaut.</span><span class="sxs-lookup"><span data-stu-id="083ca-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="083ca-124">Par exemple, si vous générez une DLL de marshaling standard comme votre propre serveur COM in-process, ou si vous devez définir votre propre **DllMain** pour gérer l' \_ attachement du processus dll \_ .</span><span class="sxs-lookup"><span data-stu-id="083ca-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="083ca-125">L’utilisation du **proxy \_ CLSID \_ est**= macro au lieu de **\_ CLSID proxy** pour définir la valeur du CLSID au format hexadécimal binaire que la macro **définir le \_ GUID** utilise.</span><span class="sxs-lookup"><span data-stu-id="083ca-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="083ca-126">Notez également que lorsque la fonction **DllRegisterServer** par défaut s’exécute, elle inscrit le serveur avec ThreadingModel = both.</span><span class="sxs-lookup"><span data-stu-id="083ca-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="083ca-127">L’exemple de fichier Make suivant utilise les macros **proxy du proxy d’inscription \_ \_** et **\_ CLSID du proxy**:</span><span class="sxs-lookup"><span data-stu-id="083ca-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="083ca-128">Pour plus d’informations sur l’option de préprocesseur [**/d**](-d.md) , consultez la documentation de votre compilateur C.</span><span class="sxs-lookup"><span data-stu-id="083ca-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 





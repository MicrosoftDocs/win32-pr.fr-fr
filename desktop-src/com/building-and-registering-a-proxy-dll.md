---
title: Génération et inscription d’une DLL proxy
description: Si vous avez choisi le marshaling proxy/stub pour votre application, les fichiers. c et. h que MIDL a générés doivent être compilés et liés pour créer une DLL de proxy, et cette DLL doit être entrée dans le registre système afin que les clients puissent localiser vos interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730516"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="acc18-103">Génération et inscription d’une DLL proxy</span><span class="sxs-lookup"><span data-stu-id="acc18-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="acc18-104">Si vous avez choisi le marshaling proxy/stub pour votre application, les fichiers. c et. h que MIDL a générés doivent être compilés et liés pour créer une DLL de proxy, et cette DLL doit être entrée dans le registre système afin que les clients puissent localiser vos interfaces.</span><span class="sxs-lookup"><span data-stu-id="acc18-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="acc18-105">Le fichier généré par MIDL dlldata. c contient les routines nécessaires et d’autres informations pour créer et inscrire une DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="acc18-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="acc18-106">La première étape de la création de la DLL consiste à écrire un fichier de définition de module pour l’éditeur de liens, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="acc18-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="acc18-107">Vous pouvez également spécifier ces fonctions exportées sur la ligne de commande LINK de votre Makefile.</span><span class="sxs-lookup"><span data-stu-id="acc18-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="acc18-108">Les fonctions exportées sont déclarées dans rpcproxy. h, qui est inclus dans dlldata. c, et les implémentations par défaut font partie de la bibliothèque Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="acc18-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="acc18-109">COM utilise ces fonctions pour créer une fabrique de classes, décharger les dll (après avoir vérifié qu’il n’existe aucun objet ou verrou), récupérer des informations sur la DLL proxy et s’inscrire et annuler l’inscription de la DLL proxy.</span><span class="sxs-lookup"><span data-stu-id="acc18-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="acc18-110">Pour tirer parti de ces fonctions prédéfinies, vous devez appeler l’option Cpreprocessor/D (ou-D) quand vous compilez les fichiers dlldata. c et example \_ p. c, comme illustré dans le Makefile suivant :</span><span class="sxs-lookup"><span data-stu-id="acc18-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="acc18-111">Si vous ne spécifiez pas ces définitions de préprocesseur au moment de la compilation, ces fonctions ne sont pas définies automatiquement.</span><span class="sxs-lookup"><span data-stu-id="acc18-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="acc18-112">(Autrement dit, les macros dans rpcproxy. c se développent en rien.) Vous devez les définir explicitement dans un autre fichier source, dont le module serait également inclus dans la liaison et la compilation finales sur la ligne de commande du compilateur C.</span><span class="sxs-lookup"><span data-stu-id="acc18-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="acc18-113">Lorsque la \_ dll du proxy \_ d’inscription est définie, rpcproxy. h fournit un contrôle de compilation conditionnelle supplémentaire avec proxy \_ CLSID =*GUID*, le \_ CLSID \_ du proxy est =*valeur explicite du GUID* et le préfixe d’entrée \_ = chaîne de *préfixe*.</span><span class="sxs-lookup"><span data-stu-id="acc18-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="acc18-114">Ces définitions de macros sont décrites plus en détail dans les [définitions de compilateur C pour les proxys/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) dans le Guide du programmeur MIDL.</span><span class="sxs-lookup"><span data-stu-id="acc18-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="acc18-115">Inscription manuelle de la DLL du proxy</span><span class="sxs-lookup"><span data-stu-id="acc18-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="acc18-116">Si, pour une raison quelconque, vous ne pouvez pas utiliser les routines d’inscription par proxy stub, vous pouvez inscrire manuellement la DLL en ajoutant les entrées suivantes au registre système, à l’aide de Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="acc18-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="acc18-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acc18-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc18-118">C-définitions de compilateur pour les proxys/stubs</span><span class="sxs-lookup"><span data-stu-id="acc18-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="acc18-119">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="acc18-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="acc18-120">Inscription automatique</span><span class="sxs-lookup"><span data-stu-id="acc18-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 
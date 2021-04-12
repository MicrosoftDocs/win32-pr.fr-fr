---
title: Self-Registration
description: L’auto-inscription est le moyen standard par lequel un module de serveur peut empaqueter ses propres opérations de Registre, à la fois l’inscription et la désinscription, dans le module lui-même.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463763"
---
# <a name="self-registration"></a><span data-ttu-id="1a9fc-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="1a9fc-103">Self-Registration</span></span>

<span data-ttu-id="1a9fc-104">Étant donné que le logiciel de composant continue de croître sur le marché, il y aura de plus en plus d’instances où un utilisateur obtient un nouveau composant logiciel sous la forme d’un module DLL ou EXE unique, par exemple lors du téléchargement d’un nouveau composant à partir d’un service en ligne ou en recevant un à partir d’un ami sur une disquette.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="1a9fc-105">Dans ce cas, il n’est pas pratique de demander à l’utilisateur de passer par une procédure d’installation ou un programme d’installation de longue durée.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="1a9fc-106">Outre les problèmes de gestion de licences, qui sont gérés via [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), une procédure d’installation crée généralement les entrées de Registre nécessaires pour qu’un composant s’exécute correctement dans le contexte com et OLE.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="1a9fc-107">L’auto-inscription est le moyen standard par lequel un module de serveur peut empaqueter ses propres opérations de Registre, à la fois l’inscription et la désinscription, dans le module lui-même.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="1a9fc-108">Lorsqu’il est utilisé avec la gestion des licences par le biais de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un serveur peut devenir un module entièrement autonome sans avoir besoin de programmes d’installation externes ou de fichiers. reg.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="1a9fc-109">Tout module à inscription automatique, DLL ou EXE, doit tout d’abord inclure une chaîne « OleSelfRegister » dans la section [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de sa ressource d’informations de version, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

<span data-ttu-id="1a9fc-110">L’existence de ces données permet à toute partie intéressée, telle qu’une application qui souhaite intégrer ce nouveau composant, de déterminer si le serveur prend en charge l’inscription automatique sans avoir à charger d’abord la DLL ou l’EXE.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="1a9fc-111">Si le serveur est empaqueté dans un module DLL, la DLL doit exporter les fonctions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="1a9fc-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="1a9fc-112">Toute application souhaitant demander au serveur de s’inscrire lui-même (autrement dit, tous ses CLSID et ID de bibliothèque de types) peut obtenir un pointeur vers **DllRegisterServer** via la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1a9fc-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="1a9fc-113">Dans **DllRegisterServer**, la dll crée toutes les entrées de Registre nécessaires, en stockant le chemin d’accès correct à la dll pour toutes les entrées [InprocServer32](inprocserver32.md) ou [InprocHandler32](inprochandler32.md) .</span><span class="sxs-lookup"><span data-stu-id="1a9fc-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="1a9fc-114">Quand une application souhaite supprimer le composant du système, elle doit annuler l’inscription de ce composant en appelant [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="1a9fc-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="1a9fc-115">Dans cet appel, le serveur supprime exactement les entrées qu’il a créées précédemment dans [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="1a9fc-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="1a9fc-116">Le serveur ne doit pas supprimer en aveugle toutes les entrées de ses classes, car d’autres logiciels peuvent avoir stocké des entrées supplémentaires, telles qu’une clé [TreatAs](treatas.md) .</span><span class="sxs-lookup"><span data-stu-id="1a9fc-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="1a9fc-117">Si le serveur est empaqueté dans un module EXE, l’application souhaitant inscrire le serveur lance le serveur EXE avec l’argument de ligne de commande **/regserver** ou **-regserver** (non-respect de la casse).</span><span class="sxs-lookup"><span data-stu-id="1a9fc-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="1a9fc-118">Si l’application souhaite annuler l’inscription du serveur, elle lance l’EXE avec l’argument de ligne de commande **commutateur/unregserver** ou **-UnregServer**.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="1a9fc-119">Le fichier EXE auto-inscrit détecte ces arguments de ligne de commande et appelle les mêmes opérations qu’une DLL dans [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivement, en inscrivant son chemin d’accès au module sous [LocalServer32](localserver32.md) au lieu de **InprocServer32** ou **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="1a9fc-120">Le serveur doit enregistrer le chemin d’accès complet de l’emplacement d’installation du module DLL ou EXE pour leurs clés **InprocServer32**, **InprocHandler32** et **LocalServer32** respectives dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1a9fc-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="1a9fc-121">Le chemin d’accès du module est facilement obtenu via la fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="1a9fc-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a9fc-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a9fc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a9fc-123">Installation d’une application en tant que service</span><span class="sxs-lookup"><span data-stu-id="1a9fc-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="1a9fc-124">Inscription d’une classe lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="1a9fc-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="1a9fc-125">Inscription d’un serveur exécutable en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="1a9fc-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="1a9fc-126">Inscription d’objets dans le ROT</span><span class="sxs-lookup"><span data-stu-id="1a9fc-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 
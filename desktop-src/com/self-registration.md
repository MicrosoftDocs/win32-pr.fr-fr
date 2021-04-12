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
# <a name="self-registration"></a>Self-Registration

Étant donné que le logiciel de composant continue de croître sur le marché, il y aura de plus en plus d’instances où un utilisateur obtient un nouveau composant logiciel sous la forme d’un module DLL ou EXE unique, par exemple lors du téléchargement d’un nouveau composant à partir d’un service en ligne ou en recevant un à partir d’un ami sur une disquette. Dans ce cas, il n’est pas pratique de demander à l’utilisateur de passer par une procédure d’installation ou un programme d’installation de longue durée. Outre les problèmes de gestion de licences, qui sont gérés via [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), une procédure d’installation crée généralement les entrées de Registre nécessaires pour qu’un composant s’exécute correctement dans le contexte com et OLE.

L’auto-inscription est le moyen standard par lequel un module de serveur peut empaqueter ses propres opérations de Registre, à la fois l’inscription et la désinscription, dans le module lui-même. Lorsqu’il est utilisé avec la gestion des licences par le biais de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un serveur peut devenir un module entièrement autonome sans avoir besoin de programmes d’installation externes ou de fichiers. reg.

Tout module à inscription automatique, DLL ou EXE, doit tout d’abord inclure une chaîne « OleSelfRegister » dans la section [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) de sa ressource d’informations de version, comme illustré ici.

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

L’existence de ces données permet à toute partie intéressée, telle qu’une application qui souhaite intégrer ce nouveau composant, de déterminer si le serveur prend en charge l’inscription automatique sans avoir à charger d’abord la DLL ou l’EXE.

Si le serveur est empaqueté dans un module DLL, la DLL doit exporter les fonctions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Toute application souhaitant demander au serveur de s’inscrire lui-même (autrement dit, tous ses CLSID et ID de bibliothèque de types) peut obtenir un pointeur vers **DllRegisterServer** via la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) . Dans **DllRegisterServer**, la dll crée toutes les entrées de Registre nécessaires, en stockant le chemin d’accès correct à la dll pour toutes les entrées [InprocServer32](inprocserver32.md) ou [InprocHandler32](inprochandler32.md) .

Quand une application souhaite supprimer le composant du système, elle doit annuler l’inscription de ce composant en appelant [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver). Dans cet appel, le serveur supprime exactement les entrées qu’il a créées précédemment dans [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver). Le serveur ne doit pas supprimer en aveugle toutes les entrées de ses classes, car d’autres logiciels peuvent avoir stocké des entrées supplémentaires, telles qu’une clé [TreatAs](treatas.md) .

Si le serveur est empaqueté dans un module EXE, l’application souhaitant inscrire le serveur lance le serveur EXE avec l’argument de ligne de commande **/regserver** ou **-regserver** (non-respect de la casse). Si l’application souhaite annuler l’inscription du serveur, elle lance l’EXE avec l’argument de ligne de commande **commutateur/unregserver** ou **-UnregServer**. Le fichier EXE auto-inscrit détecte ces arguments de ligne de commande et appelle les mêmes opérations qu’une DLL dans [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectivement, en inscrivant son chemin d’accès au module sous [LocalServer32](localserver32.md) au lieu de **InprocServer32** ou **InprocHandler32**.

Le serveur doit enregistrer le chemin d’accès complet de l’emplacement d’installation du module DLL ou EXE pour leurs clés **InprocServer32**, **InprocHandler32** et **LocalServer32** respectives dans le registre. Le chemin d’accès du module est facilement obtenu via la fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installation d’une application en tant que service](installing-as-a-service-application.md)
</dt> <dt>

[Inscription d’une classe lors de l’installation](registering-a-class-at-installation.md)
</dt> <dt>

[Inscription d’un serveur exécutable en cours d’exécution](registering-a-running-exe-server.md)
</dt> <dt>

[Inscription d’objets dans le ROT](registering-objects-in-the-rot.md)
</dt> </dl>

 

 
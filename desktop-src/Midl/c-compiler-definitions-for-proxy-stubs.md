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
# <a name="c-compiler-definitions-for-proxystubs"></a>C-définitions de compilateur pour les proxys/stubs

Le fichier d’en-tête rpcproxy. h comprend les définitions de macro suivantes, qui peuvent être utiles lors de la création d’une application COM distribuée. Ces macros sont appelées avec le commutateur de préprocesseur [**/d**](-d.md) (ou-D) au moment de la compilation C.



| MACRO                                                                                                                                                                                           | Description                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INSCRIRE \_ la \_ dll proxy                                                                                                                                                                            | Génère des fonctions **DllMain**, **DllRegisterServer** et **DllUnregisterServer** pour l’inscription automatique d’une dll proxy.                                                                                       |
| CLSID du PROXY \_ =<clsid>                                                                                                                                                                      | Spécifie un identificateur de classe pour le serveur. Si cette macro n’est pas définie, le CLSID par défaut est le premier identificateur d’interface que le compilateur MIDL rencontre dans la spécification IDL pour le serveur proxy/stub. |
| Le \_ CLSID du proxy \_ est = {0x *8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*,}} | Spécifie la valeur de l’identificateur de classe du serveur au format hexadécimal binaire.                                                                                                                                           |



 

En définissant la macro **\_ \_ dll du proxy d’inscription** lors de la compilation de dlldata. c, votre dll de marshaling de proxy/stub inclut automatiquement les définitions par défaut des fonctions **DllMain**, **DllRegisterServer** et **DllUnregisterServer** . Vous pouvez utiliser ces fonctions pour enregistrer automatiquement votre DLL de proxy dans le registre système.

Ce code d’inscription par défaut utilise le GUID de la première interface rencontrée comme CLSID pour l’inscription de l’intégralité du serveur DLL proxy/stub. Par la suite, COM utilise ce CLSID pour localiser et charger le serveur proxy/stub compilé pour le marshaling des interfaces que le serveur est inscrit pour gérer. Lorsqu’une application effectue un appel de méthode d’interface qui franchit les limites du thread, du processus ou de l’ordinateur, COM utilise l’entrée du registre de l’identificateur d’interface pour localiser l’entrée de Registre CLSID pour le serveur de marshaling proxy/stub. Il utilise ensuite ce CLSID pour charger le serveur (s’il n’est pas déjà chargé) afin que l’appel d’interface puisse être marshalé.

Utilisez la macro **proxy \_ CLSID** = <clsid> lorsque vous souhaitez spécifier explicitement le CLSID du serveur proxy/stub au lieu de s’appuyer sur le CLSID par défaut. Par exemple, si vous générez une DLL de marshaling standard comme votre propre serveur COM in-process, ou si vous devez définir votre propre **DllMain** pour gérer l' \_ attachement du processus dll \_ .

L’utilisation du **proxy \_ CLSID \_ est**= macro au lieu de **\_ CLSID proxy** pour définir la valeur du CLSID au format hexadécimal binaire que la macro **définir le \_ GUID** utilise.

Notez également que lorsque la fonction **DllRegisterServer** par défaut s’exécute, elle inscrit le serveur avec ThreadingModel = both.

L’exemple de fichier Make suivant utilise les macros **proxy du proxy d’inscription \_ \_** et **\_ CLSID du proxy**:

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

Pour plus d’informations sur l’option de préprocesseur [**/d**](-d.md) , consultez la documentation de votre compilateur C.

 

 





---
title: Génération et inscription d’une DLL proxy
description: Si vous avez choisi le marshaling proxy/stub pour votre application, les fichiers. c et. h que MIDL a générés doivent être compilés et liés pour créer une DLL de proxy, et cette DLL doit être entrée dans le registre système afin que les clients puissent localiser vos interfaces.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634cb7a17551a4b7925d0be3065c71037cc1d7ae8bf28c10fcdaee74771c302e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048847"
---
# <a name="building-and-registering-a-proxy-dll"></a>Génération et inscription d’une DLL proxy

Si vous avez choisi le marshaling proxy/stub pour votre application, les fichiers. c et. h que MIDL a générés doivent être compilés et liés pour créer une DLL de proxy, et cette DLL doit être entrée dans le registre système afin que les clients puissent localiser vos interfaces. Le fichier généré par MIDL dlldata. c contient les routines nécessaires et d’autres informations pour créer et inscrire une DLL proxy/stub.

La première étape de la création de la DLL consiste à écrire un fichier de définition de module pour l’éditeur de liens, comme indiqué dans l’exemple suivant :

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

Vous pouvez également spécifier ces fonctions exportées sur la ligne de commande LINK de votre Makefile.

Les fonctions exportées sont déclarées dans rpcproxy. h, qui est inclus dans dlldata. c, et les implémentations par défaut font partie de la bibliothèque Runtime RPC. COM utilise ces fonctions pour créer une fabrique de classes, décharger les dll (après avoir vérifié qu’il n’existe aucun objet ou verrou), récupérer des informations sur la DLL proxy et s’inscrire et annuler l’inscription de la DLL proxy. Pour tirer parti de ces fonctions prédéfinies, vous devez appeler l’option Cpreprocessor/D (ou-D) quand vous compilez les fichiers dlldata. c et example \_ p. c, comme illustré dans le Makefile suivant :

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
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

Si vous ne spécifiez pas ces définitions de préprocesseur au moment de la compilation, ces fonctions ne sont pas définies automatiquement. (Autrement dit, les macros dans rpcproxy. c se développent en rien.) Vous devez les définir explicitement dans un autre fichier source, dont le module serait également inclus dans la liaison et la compilation finales sur la ligne de commande du compilateur C.

Lorsque la \_ dll du proxy \_ d’inscription est définie, rpcproxy. h fournit un contrôle de compilation conditionnelle supplémentaire avec proxy \_ CLSID =*GUID*, le \_ CLSID \_ du proxy est =*valeur explicite du GUID* et le préfixe d’entrée \_ = chaîne de *préfixe*. Ces définitions de macros sont décrites plus en détail dans les [définitions de compilateur C pour les proxys/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) dans le Guide du programmeur MIDL.

## <a name="manually-registering-the-proxy-dll"></a>Inscription manuelle de la DLL du proxy

Si, pour une raison quelconque, vous ne pouvez pas utiliser les routines d’inscription par proxy stub, vous pouvez inscrire manuellement la DLL en ajoutant les entrées suivantes au registre système, à l’aide de Regedt32.exe.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[C-définitions de compilateur pour les proxys/stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[Inscription automatique](self-registration.md)
</dt> </dl>

 

 

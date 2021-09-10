---
title: Création de la table d’interface globale
description: Création de la table d’interface globale
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363348"
---
# <a name="creating-the-global-interface-table"></a>Création de la table d’interface globale

Utilisez l’appel suivant pour créer l’objet de table d’interface globale et obtenir un pointeur vers [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> Lors de la création de l’objet table d’interface globale à l’aide de l’appel précédent, il est nécessaire de créer un lien vers la bibliothèque UUID. lib. Cela permet de résoudre les symboles externes CLSID \_ StdGlobalInterfaceTable et IID \_ IGlobalInterfaceTable.

 

Comme il existe une seule instance de la table d’interface globale par processus, tous les appels à cette fonction dans un processus retournent la même instance.

Après l’appel à la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , inscrivez l’interface à partir du cloisonnement dans lequel elle réside avec un appel à la méthode [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) . Cette méthode fournit un cookie qui identifie l’interface et son emplacement. Un cloisonnement qui recherche un pointeur vers cette interface appelle ensuite la méthode [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) avec ce cookie, et l’implémentation fournit ensuite un pointeur d’interface vers le cloisonnement appelant. Pour révoquer l’inscription globale de l’interface, tout cloisonnement peut appeler la méthode [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .

Un exemple simple d’utilisation de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) serait lorsque vous souhaiterez passer un pointeur d’interface sur un objet dans un thread cloisonné (STA) à un thread de travail dans un autre cloisonnement. Plutôt que d’avoir à les marshaler dans un flux et à passer le flux au thread de travail en tant que paramètre de thread, **IGlobalInterfaceTable** vous permet simplement de passer un cookie.

Lorsque vous inscrivez l’interface dans la table d’interface globale, vous recevez un cookie que vous pouvez utiliser au lieu de passer le pointeur réel (chaque fois que vous devez passer le pointeur) à un paramètre de non-méthode qui passe à un autre cloisonnement (en tant que paramètre de [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) via [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) ou à la mémoire en cours d’exécution accessible en dehors de votre cloisonnement.

La prudence est nécessaire, car l’utilisation d’interfaces globales place la charge supplémentaire sur le programmeur de gestion des problèmes tels que les conditions de concurrence et l’exclusion mutuelle, qui sont associées à l’accès à l’état global à partir de plusieurs threads simultanément.

COM fournit une implémentation standard de l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Il est vivement recommandé d’utiliser cette implémentation standard, car elle fournit une fonctionnalité thread-safe complète.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Quand utiliser la table d’interface globale](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 
---
title: Quand utiliser la table d’interface globale
description: Quand utiliser la table d’interface globale
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013043"
---
# <a name="when-to-use-the-global-interface-table"></a>Quand utiliser la table d’interface globale

Si vous démarshalez plusieurs fois un pointeur d’interface entre des cloisonnements dans un processus, vous pouvez utiliser l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Avec d’autres techniques, vous devez remarshaler chaque fois.

> [!Note]  
> Si le pointeur d’interface n’est démarshalé qu’une seule fois, vous souhaiterez peut-être utiliser la fonction [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) . Elle peut également être utilisée pour passer un pointeur d’interface d’un thread à un autre dans le même processus.

 

L’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) complique également un autre problème précédemment difficile pour le programmeur. Ce problème se produit lorsque les conditions suivantes s’appliquent :

-   Un objet agile in-process agrège le marshaleur libre de threads.
-   Ce même objet agile contient également des pointeurs d’interface (comme variables membres) vers d’autres objets qui ne sont pas agiles et qui n’agrègent pas le marshaleur libre de threads.

Dans ce cas, si l’objet externe est marshalé vers un autre cloisonnement et que l’application y appelle, et que l’objet tente d’appeler sur l’un de ses pointeurs d’interface de variable membre qui ne sont pas libres de threads ou qui sont des proxies vers des objets d’autres Apartments, il peut obtenir des résultats incorrects ou le \_ thread RPC E \_ incorrect \_ . Cette erreur se produit parce que l’interface interne est conçue pour être appelée uniquement à partir du cloisonnement dans lequel elle a été stockée pour la première fois dans la variable membre.

Pour résoudre ce problème, l’objet externe qui agrège le marshaleur libre de threads doit appeler [**IGlobalInterfaceTable :: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) sur l’interface interne et stocker le cookie résultant dans sa variable membre, au lieu de stocker le pointeur d’interface réel. Lorsque l’objet externe souhaite appeler sur le pointeur d’interface d’un objet interne, il doit appeler [**IGlobalInterfaceTable :: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), utiliser le pointeur d’interface retourné, puis le libérer. Lorsque l’objet externe disparaît, il doit appeler [**IGlobalInterfaceTable :: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) pour supprimer l’interface de la table d’interface globale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de la table d’interface globale](creating-the-global-interface-table.md)
</dt> </dl>

 

 
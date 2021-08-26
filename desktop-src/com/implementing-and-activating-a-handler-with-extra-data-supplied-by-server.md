---
title: Implémentation et activation d’un gestionnaire avec des données supplémentaires fournies par le serveur
description: Implémentation et activation d’un gestionnaire avec des données supplémentaires fournies par le serveur
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4777c44dd9983a0193872507272862766c51e708f5caa491a6f8d787923749c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029925"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implémentation et activation d’un gestionnaire avec des données supplémentaires fournies par le serveur

Si le serveur souhaite inclure des données supplémentaires dans le paquet à utiliser par le gestionnaire, le serveur doit implémenter les interfaces [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) et [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) . Le serveur doit agréger le marshaleur standard et doit déléguer la première partie du marshaling au marshaleur standard agrégé, y compris [**IMarshal :: GetUnmarshalClass**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass), et doit ajouter sa propre taille de données à la taille retournée par le [**IMarshal :: GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)du marshaleur standard. Le marshaleur standard appelle [**IStdMarshalInfo :: GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) pour récupérer le CLSID du gestionnaire à créer. Une fois que le marshaleur standard a effectué son marshaling, le serveur écrit ses propres données supplémentaires dans le flux. Les structures résultantes, avec des données supplémentaires dans le flux, sont affichées dans l’illustration suivante :

![Diagramme qui affiche des structures avec des données supplémentaires dans le flux.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side les structures avec des données supplémentaires dans le flux

Cela permet à l’appel de COM à [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) côté client d’ignorer les données non lues et de conserver le flux dans la position appropriée qui suit toutes les données d’interface marshalées si le gestionnaire ne peut pas être créé.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side les structures avec des données supplémentaires dans le flux

Comme dans le cas où il n’y a pas de données serveur supplémentaires dans le flux, l’appel COM côté client à [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) créera l’identité et le gestionnaire. Le gestionnaire doit implémenter [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) et doit déléguer d’abord les appels **IMarshal** au marshaleur standard agrégé, puis marshaler ou démarshaler les données supplémentaires fournies par le serveur. Le [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) du gestionnaire sera appelé pour chaque unmarshalé, qu’il ait ou non marshalé l’interface. Dans ce cas, le serveur n’appelle pas [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) , mais le gestionnaire doit le faire. La structure résultante côté client est présentée dans l’illustration suivante.

![Diagramme qui montre la structure côté client.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de Client-Side léger](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 
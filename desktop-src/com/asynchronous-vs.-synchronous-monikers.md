---
title: Monikers asynchrones et synchrones
description: Monikers asynchrones et synchrones
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232769"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Monikers asynchrones et synchrones

Un client d’un moniker OLE synchrone standard crée et contient généralement une référence au moniker, ainsi que le contexte de liaison à utiliser pendant la liaison. Les composants impliqués dans l’utilisation des monikers traditionnels sont illustrés dans le diagramme suivant.

![Diagramme qui montre le client connecté à un contexte de liaison ou à n’importe quel moniker du fourni par le système.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

Les clients créent généralement des monikers standard en appelant des fonctions telles que [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)ou [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) ou, car ils peuvent être enregistrés dans un stockage persistant, via [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) et [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). Les monikers peuvent également être obtenus à partir d’un objet conteneur en appelant la méthode [**IBindHost :: CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) . Les clients créent des contextes de liaison en appelant la fonction [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) , puis transmettent le contexte de liaison au moniker avec des appels à [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Comme indiqué dans le diagramme suivant, un client d’un moniker asynchrone crée également et contient une référence au moniker et au contexte de liaison à utiliser pendant la liaison.

![Diagramme qui montre les connexions entre le fourni par le client, fourni par Monker et fourni par le système.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Pour obtenir un comportement asynchrone, le client implémente l’interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) sur un objet bind-statue-callback et appelle la fonction [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) ou la fonction [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) pour inscrire cette interface avec le contexte de liaison. Le moniker passe un pointeur vers son interface [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) dans un appel à la méthode [**IBindStatusCallback :: OnStartBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) . Le client indique au moniker asynchrone comment il souhaite effectuer une liaison au retour de l’appel du moniker à la méthode [**IBindStatusCallback :: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers asynchrones](asynchronous-monikers.md)
</dt> </dl>

 

 
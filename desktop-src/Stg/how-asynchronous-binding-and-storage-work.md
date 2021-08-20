---
title: fonctionnement de la liaison asynchrone et du Stockage
description: Le stockage asynchrone améliore la spécification de stockage structuré COM afin de prendre en charge le téléchargement d’objets de stockage sur des réseaux à latence élevée et de liaison lente tels qu’Internet.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- fonctionnement de la liaison asynchrone et du Stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176ff85044210a94cecf2649fa7475eae2b291def43b0876d2ecbc9c98b0866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961899"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>fonctionnement de la liaison asynchrone et du Stockage

Le stockage asynchrone améliore la spécification de stockage structuré COM afin de prendre en charge le téléchargement d’objets de stockage sur des réseaux à latence élevée et de liaison lente tels qu’Internet. Le stockage asynchrone fonctionne avec les monikers asynchrones pour fournir un comportement de liaison asynchrone complet.

## <a name="document-object-embedded-in-a-web-page"></a>Objet document incorporé dans une page Web

Lorsqu’un utilisateur clique sur un lien représentant un document incorporé dans une page Web, les événements suivants se produisent :

1.  Le navigateur appelle la fonction [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) , en passant l’URL du lien.
2.  [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) analyse l’URL, crée un moniker asynchrone correspondant et retourne un pointeur vers l’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) du moniker.
3.  Le navigateur appelle [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) pour déterminer si le moniker est asynchrone, crée un contexte de liaison, inscrit l’interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) avec le contexte de liaison, uniquement si le moniker est asynchrone et appelle [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), en passant le contexte de liaison.
4.  Le moniker est lié à l’objet et le interroge pour l’interface [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , qui indique si l’objet prend en charge la liaison asynchrone et le stockage. Si l’objet retourne un pointeur vers **IPersistMoniker**:

    1.  Le moniker d’URL appelle [**IPersistMoniker :: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)), en passant son propre pointeur [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) à l’objet.
    2.  L’objet modifie le contexte de liaison, choisit s’il souhaite un stockage bloquant ou non bloquant, inscrit son propre [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) et appelle [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) sur le pointeur qu’il a reçu via [**IPersistMoniker :: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  Le moniker crée un stockage asynchrone, conserve une référence à l’interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) de l’objet wrapper, inscrit l’interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) sur le stockage racine et appelle [**IPersistStorage :: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), en passant le pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) du stockage asynchrone. À mesure que les données arrivent (sur un thread d’arrière-plan), le moniker appelle **IFillLockBytes** pour remplir l' [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sur le fichier temporaire.
    4.  L’objet lit les données à partir du stockage et retourne à partir de [**IPersistMoniker :: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) lorsqu’il a reçu suffisamment de données pour s’en tenir initialisé. Si l’objet tente de lire des données qui n’ont pas encore été téléchargées, le téléchargeur reçoit une notification sur [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). À l’intérieur de la méthode [**IProgressNotify :: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , le thread de téléchargement bloque une boucle de messages modale ou fait en sorte que le stockage asynchrone retourne E \_ en attente, selon que l’objet a demandé ou non un stockage de blocage ou de non-blocage.

5.  Si l’objet n’implémente pas [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), le moniker interroge la pour [**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), qui indique que l’état persistant de l’objet est stocké dans un objet de stockage. Si l’objet retourne un pointeur vers **IPersistStorage**:

    1.  Le moniker appelle [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) sur lui-même, en demandant un blocage [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (car l’objet ne prend pas en charge asynchrone), crée un stockage asynchrone, conserve une référence à l’interface [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) de l’objet wrapper, inscrit l’interface [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) sur le stockage racine et appelle [**IPersistStorage :: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), en passant le pointeur **IStorage** de stockage asynchrone. À mesure que les données arrivent (sur un thread d’arrière-plan), le moniker appelle [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) pour remplir l' [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sur le fichier temporaire.
    2.  L’objet lit les données à partir du stockage et retourne de [**IPersistStorage :: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) lorsqu’il a reçu suffisamment de données pour être initialisées. Si l’objet tente de lire des données qui n’ont pas encore été téléchargées, il reçoit une notification sur [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). À l’intérieur de la méthode [**IProgressNotify :: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) , le thread de téléchargement se bloque toujours dans une boucle de messages modale.

6.  Que le téléchargement soit synchrone ou asynchrone, le moniker retourne de [**IMoniker :: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), et le navigateur reçoit l’objet initialisé qu’il a demandé.
7.  Le navigateur interroge [**IOleObject**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) et héberge l’objet sous la forme d’un objet document. (À ce stade, l’objet ne peut pas être initialisé complètement, mais suffisant pour afficher un résultat utile, auquel cas le téléchargement se poursuit en arrière-plan.)

 

 
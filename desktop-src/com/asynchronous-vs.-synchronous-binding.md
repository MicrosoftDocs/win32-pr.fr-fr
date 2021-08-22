---
title: Liaison asynchrone et synchrone
description: Liaison asynchrone et synchrone
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048857"
---
# <a name="asynchronous-and-synchronous-binding"></a>Liaison asynchrone et synchrone

Le client peut vérifier si le moniker est asynchrone en appelant la fonction [**IsAsyncMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) . Si le client retourne l' \_ indicateur asynchrone BINDF, plutôt que de retourner un pointeur d’objet ou un pointeur de stockage à partir d’appels suivants à [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) ou [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), le moniker retourne MK \_ S \_ asynchrone à la place du pointeur d’objet et **null** à la place du pointeur de stockage. En réponse, le client doit attendre de recevoir l’objet ou le stockage demandé pendant l’implémentation de [**IBindStatusCallback :: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) et [**IBindStatusCallback :: OnObjectAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

L’objet de rappel reçoit également une notification de progression via [**IBindStatusCallback :: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), une notification de disponibilité des données via [**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))et d’autres notifications du moniker sur l’état de l’opération de liaison.

Si le client ne retourne pas l' \_ indicateur asynchrone BINDF à partir de l’appel du moniker à [**IBindStatusCallback :: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), l’opération de liaison se poursuit de façon synchrone et l’objet ou le stockage souhaité est retourné à partir des appels suivants à [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ou [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage). De même, si le client souhaite une opération synchrone et ne souhaite pas recevoir de notifications de progression ou de rappels, il peut demander à un moniker asynchrone de se comporter de façon synchrone en n’implémentant pas [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). Dans ce cas, le moniker asynchrone se comporte comme un moniker synchrone standard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers asynchrones](asynchronous-monikers.md)
</dt> </dl>

 

 
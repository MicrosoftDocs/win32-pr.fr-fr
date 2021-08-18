---
description: Définit une méthode qui détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.
title: " IStorageProviderCopyHook"
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: aa26a329bd80295a6a46a1bb11d1dc651baf1ea71975576ed704b29a7fee8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968868"
---
# <a name="istorageprovidercopyhook-interface"></a> IStorageProviderCopyHook

Expose une méthode qui détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.

## <a name="members"></a>Membres

L’interface **IStorageProviderCopyHook** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IStorageProviderCopyHook** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IStorageProviderCopyHook** possède ces méthodes.



| Méthode                                           | Description                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.                                                           |


## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 10 Version préliminaire d’Insider 19624                                                |
| En-tête<br/>                   | ShObjIdl. h   |

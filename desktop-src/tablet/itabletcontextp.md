---
description: Représente le contexte de tablette.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interface ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532303"
---
# <a name="itabletcontextp-interface"></a>Interface ITabletContextP

Représente le contexte de tablette.

## <a name="members"></a>Membres

L’interface **ITabletContextP** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletContextP** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITabletContextP** possède ces méthodes.



| Méthode                                                                                           | Description                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | Indique si le contexte de tablette se trouve dans le hook le plus élevé.<br/>             |
| [**Éviter**](itabletcontextp-overlap.md)                                                       | Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Fournit l’accès à la mémoire partagée entre les Tablet threads.<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | Fournit l’accès à la mémoire partagée entre les Tablet threads.<br/>             |



 

## <a name="remarks"></a>Notes

Les développeurs ne doivent pas utiliser cette interface.

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) est disponible uniquement sur Windows Vista et versions ultérieures.

Le code suivant décrit comment l’interface **ITabletContextP** est définie.

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 


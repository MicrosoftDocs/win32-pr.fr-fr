---
description: Représente une tablette attachée à l’ordinateur.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interface ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a0cb98a74758d701e7ab6322567d2a20606380a58fc43676ad5edb136cec999b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712249"
---
# <a name="itablet-interface"></a>Interface ITablet

Représente une tablette attachée à l’ordinateur.

## <a name="members"></a>Membres

L’interface **ITablet** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITablet** possède ces méthodes.



| Méthode                                                                 | Description                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Crée un objet de contexte qui décrit le périphérique tablette spécifié.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Récupère l’objet [**ITabletCursor**](itabletcursor.md) spécifié.<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | Récupère le nombre d’objets Cursor associés à la tablette.<br/>         |
| [**GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md) | Récupère les paramètres de contexte par défaut pour la tablette.<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | Récupère une valeur qui représente les fonctionnalités du matériel de tablette.<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Récupère une chaîne contenant le nom du périphérique tablette.<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | Récupère une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Récupère les données de métriques pour une propriété spécifiée.<br/>                       |



 

## <a name="remarks"></a>Remarques

Les développeurs ne doivent pas utiliser cette interface.

Le code suivant décrit comment l’interface **ITablet** est définie.

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 


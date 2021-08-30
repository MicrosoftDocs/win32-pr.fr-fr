---
description: Rappel pour retourner les données de la table d’objets.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IObjectTableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0af1f4332f97dd0a708d37611d7a9d1c111af734
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786485"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span id="vspixengine.iobjecttablecallback"></span>Interface IObjectTableCallback

Rappel pour retourner les données de la table d’objets.

## <a name="members"></a>Membres

L’interface **IObjectTableCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IObjectTableCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Méthodes

L’interface **IObjectTableCallback** possède ces méthodes.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Méthode</th><th >Description</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></td><td ><p>Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></td><td ><p>Fonction de rappel utilisée pour informer l’hôte des informations de la table objet.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 

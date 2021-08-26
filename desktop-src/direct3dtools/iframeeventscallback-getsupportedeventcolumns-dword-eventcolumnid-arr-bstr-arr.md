---
description: Obtient des informations sur les colonnes (types de données d’événement) prises en charge par la liste d’événements.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsCallback :: GetSupportedEventColumns, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b8f0443f47f3eca96388fd1df5ed91f8c05efe10
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630818"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback :: GetSupportedEventColumns, méthode

Obtient des informations sur les colonnes (types de données d’événement) prises en charge par la liste d’événements.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a>Paramètres

*numColumns*   
Nombre de colonnes prises en charge par

*count0 \_ PID*   
ID de chaque colonne prise en charge par la liste des événements.

*count0 \_ pBstrNames*   
Noms de chaque colonne, sous la forme d’une chaîne COM, pris en charge par la liste des événements.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IFrameEventsCallback**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 

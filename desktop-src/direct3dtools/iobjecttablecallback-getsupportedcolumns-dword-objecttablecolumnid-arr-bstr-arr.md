---
description: Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableCallback :: GetSupportedColumns, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f785c8fafadf62a874d6be1d4c3ab2092f9cdaf8b49cc40f826b42fb69ce3b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283234"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback :: GetSupportedColumns, méthode

Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Paramètres

*numColumns*   
Nombre de colonnes prises en charge par la table des objets.

*count0_pIDs*   
ID de chaque colonne prise en charge par la table des objets.

*count0_pBstrNames*   
Noms de chaque colonne, sous la forme d’une chaîne COM, pris en charge par la table des objets.

## <a name="return-value"></a>Valeur renvoyée

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IObjectTableCallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 

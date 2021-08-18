---
description: Fonction de rappel utilisée pour informer l’hôte des interfaces prises en charge.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IVersionCallback :: VersionTableReady, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7397d041ebd8dc15a373f1278e3458e3d7b67b1efc3b0b1856fb886e03f487fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985529"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback :: VersionTableReady, méthode

Fonction de rappel utilisée pour informer l’hôte des interfaces prises en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a>Paramètres

*count1 \_ interfaceIds*   
Tableau contenant les GUID des ID d’interface pris en charge.

*saut*   
Nombre de GUID transmis dans count1 \_ interfaceIds.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IVersionCallback**](/windows/desktop/direct3dtools/iversioncallback)

 

 

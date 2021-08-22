---
description: Met à jour l’état initial d’un objet ; par exemple, une texture ou un nuanceur.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine4 :: UpdateObject, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27bd0d8aa7580884a1b4bff6b38bf032cf39b5bd4d21f5330ff088560542c851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484709"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4 :: UpdateObject, méthode

Met à jour l’état initial d’un objet ; par exemple, une texture ou un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a>Paramètres

*objectAddress*   
ID de l’objet à mettre à jour.

*corps*   
Taille de la charge utile de mise à jour en octets.

*\_mémoire tampon count1*   
Charge utile de mise à jour.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine4**](/windows/desktop/direct3dtools/ipixengine4)

 

 

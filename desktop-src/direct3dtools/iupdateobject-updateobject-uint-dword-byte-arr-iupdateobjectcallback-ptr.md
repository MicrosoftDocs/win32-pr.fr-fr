---
description: Demande de mise à jour de l’état initial d’un objet ; par exemple, une texture ou un nuanceur.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IUpdateObject :: UpdateObject, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b48e206d09c784ac2f2df31eeab0d65cac04f740a66874fe9e436f96b8349143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282273"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject :: UpdateObject, méthode

Demande de mise à jour de l’état initial d’un objet ; par exemple, une texture ou un nuanceur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a>Paramètres

*objectAddress*   
ID de l’objet à mettre à jour.

*corps*   
Taille de la charge utile de mise à jour en octets.

*\_mémoire tampon count1*   
Charge utile de mise à jour.

*pCallback*   
Adresse d’une fonction utilisée pour notifier l’hôte que l’objet a été mis à jour.

## <a name="return-value"></a>Valeur renvoyée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IUpdateObject**](/windows/desktop/direct3dtools/iupdateobject)

 

 

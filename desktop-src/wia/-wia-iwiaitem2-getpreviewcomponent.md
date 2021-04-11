---
description: Obtient le composant WIA (Windows Image Acquisition) 2,0 Preview.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'IWiaItem2 :: GetPreviewComponent, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113306"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>IWiaItem2 :: GetPreviewComponent, méthode

Obtient le composant WIA (Windows Image Acquisition) 2,0 Preview.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Non utilisé. Définit la valeur 0.

</dd> <dt>

*ppWiaPreview* \[ à\]
</dt> <dd>

Type : **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Retourne l’adresse d’un pointeur vers l’interface [**IWiaPreview**](-wia-iwiapreview.md) du composant d’aperçu.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Utilisez cette fonction pour retourner un pointeur vers l’adresse du composant WIA 2,0 Preview pour tout objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence d’objets d’un périphérique matériel WIA 2,0.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppWiaPreview* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 

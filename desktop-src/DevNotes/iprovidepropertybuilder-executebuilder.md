---
description: Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.
ms.assetid: 4d855aed-aaa1-4cc8-be9d-1175c254a813
title: 'IProvidePropertyBuilder :: ExecuteBuilder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.ExecuteBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: c37c2a4ca1003bd701ea141f1723f4ca16aa69c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530410"
---
# <a name="iprovidepropertybuilderexecutebuilder-method"></a>IProvidePropertyBuilder :: ExecuteBuilder, méthode

Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void ExecuteBuilder(
  [in]          LONG      dispid,
  [in]          BSTR      bstrGuidBldr,
  [in]          IDispatch *pdispApp,
  [in]          LONG_PTR  hwndBldrOwner,
  [in, out]     LPVARIANT pvarValue,
  [out, retval] LPBOOL    pbActionCommitted
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DISPID* \[ dans\]
</dt> <dd>

DISPID de la propriété pour laquelle le générateur s’affiche.

</dd> <dt>

*bstrGuidBldr* \[ dans\]
</dt> <dd>

**BSTR** du GUID du générateur à appeler. Elle est retournée par [**MapToPropertyBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).

</dd> <dt>

*pdispApp* \[ dans\]
</dt> <dd>

Affectez la valeur **null**.

</dd> <dt>

*hwndBldrOwner* \[ dans\]
</dt> <dd>

Handle vers la fenêtre du générateur de fenêtres publicitaires parente.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

Valeur actuelle de la propriété. Cette valeur peut être modifiée par l’objet et remplacée par la nouvelle valeur si *pbActionCommitted* a la valeur **true**.

</dd> <dt>

*pbActionCommitted* \[ out, retval\]
</dt> <dd>

Valeur qui indique si le générateur A effectué une action sur l’objet. Peut être utilisé lorsqu’un utilisateur modifie un événement, puis appuie sur OK dans la boîte de dialogue du générateur de fenêtres publicitaires.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 





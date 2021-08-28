---
description: Vérifie si un générateur doit être associé à une propriété particulière.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'IProvidePropertyBuilder :: MapPropertyToBuilder, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 35ff9e82164251c4490355bbf0499b7fa690415d388b95f7f9c7fd0e6bd7dd3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001689"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>IProvidePropertyBuilder :: MapPropertyToBuilder, méthode

Vérifie si un générateur doit être associé à une propriété particulière.

## <a name="syntax"></a>Syntaxe


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DISPID* \[ dans\]
</dt> <dd>

DISPID de la propriété en question.

</dd> <dt>

*pdwCtlBldType* \[ à\]
</dt> <dd>

Générateur à mapper. Ce paramètre peut être une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                          | Signification                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Appeler un générateur de système standard (non pris en charge dans Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Appelle un générateur personnalisé.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | Le concepteur modifie l'objet. Il s'agit d'un comportement commun.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ à\]
</dt> <dd>

GUID qui identifie le générateur pour cette propriété.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Ce paramètre a la **valeur true** si cette propriété prend actuellement en charge un générateur.

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

 

 





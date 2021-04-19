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
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532753"
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

 

 





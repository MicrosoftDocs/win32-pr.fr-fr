---
title: Méthode INapComponentConfig InvokeUI (NapCommon. h)
description: Lance une interface utilisateur personnalisée pour un composant de programme de validation d’intégrité système (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Méthode InvokeUI NAP
- Méthode InvokeUI NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0983c01ae1adc86b54eca3c958942aab9b5c832c8cac3b2c8a0b9352b7d96b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686498"
---
# <a name="inapcomponentconfiginvokeui-method"></a>INapComponentConfig :: InvokeUI, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **InvokeUI** lance une interface utilisateur personnalisée pour un composant de programme de validation d’intégrité système (SHV).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente ou propriétaire. Un handle de fenêtre valide doit être fourni.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>       | Le SHV ne prend pas en charge une interface utilisateur personnalisée.<br/>               |



 

## <a name="remarks"></a>Remarques

Cet appel de méthode doit être bloqué jusqu’à ce que l’interface utilisateur SHV se termine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 






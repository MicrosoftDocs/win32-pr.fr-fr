---
title: Méthode INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de réinitialiser le magasin SHV à son état d’origine après l’installation.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Méthode DeleteAllConfig NAP
- Méthode DeleteAllConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843337"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3 ::D méthode eleteAllConfig

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **DeleteAllConfig** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de réinitialiser le magasin SHV à son état d’origine après l’installation. Toutes les données de configuration, à l’exception de la configuration par défaut, doivent être supprimées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                           | Description                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | L'opération a réussi.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 






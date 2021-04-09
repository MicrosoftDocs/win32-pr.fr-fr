---
title: Méthode INapComponentConfig3 NewConfig (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Méthode NewConfig NAP
- Méthode NewConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103297"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3 :: NewConfig, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **newconfig** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique. Lorsque cette fonction est appelée, un SHV doit allouer de nouvelles données de configuration et les remplir avec une copie des données de configuration par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configID* 
</dt> <dd>

Valeur qui représente la configuration. *ConfigId* est attribué par le service NPS (Network Policy Server) et est unique dans la SHV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                                 | Description                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | L'opération a réussi.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigId* est égal à 0 (valeur réservée pour la configuration par défaut).<br/>                  |
| <dl> <dt>**la \_ configuration NAP E \_ SHV \_ \_ existait**</dt> </dl> | *ConfigId* existe déjà. La liste des ID connus du serveur NPS est différente de la SHV.<br/> |



 

## <a name="remarks"></a>Notes

Une fois la nouvelle configuration créée par **newconfig**, les méthodes [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)et [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) doivent être utilisées pour modifier la configuration en fonction des besoins.

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

 

 






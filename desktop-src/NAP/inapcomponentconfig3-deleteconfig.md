---
title: Méthode INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Méthode DeleteConfig NAP
- Méthode DeleteConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740948"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3 ::D méthode eleteConfig

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **DeleteConfig** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique. L’ID peut être réutilisé une fois que les données de configuration ont été supprimées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configID* 
</dt> <dd>

Valeur qui représente les données de configuration à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                                    | Description                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | L'opération a réussi.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *ConfigId* est égal à 0 (valeur réservée pour la configuration par défaut).<br/> |
| <dl> <dt>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</dt> </dl> | *ConfigId* introuvable.<br/>                                       |



 

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

 

 






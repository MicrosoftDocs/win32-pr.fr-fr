---
title: Méthode INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Méthode GetConfigFromID NAP
- Méthode GetConfigFromID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638704b5706b68b67f854a6a52b6c845be3fb757b596e9f5425f315c7d679fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368376"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3 :: GetConfigFromID, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetConfigFromID** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configID* \[ dans\]
</dt> <dd>

Valeur qui représente la configuration. Si *configId* a la **valeur 0**, le validateur doit retourner les données de configuration par défaut dans les *données de données*.

</dd> <dt>

*nombre* \[ à\]
</dt> <dd>

Taille, en octets, des données de configuration retournées dans les *données de données*.

</dd> <dt>

*données* \[ de l' à\]
</dt> <dd>

Au retour, tableau d’octets qui contient les données de configuration représentées par *configId*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                                    | Description                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | L'opération a réussi.<br/> |
| <dl> <dt>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</dt> </dl> | *ConfigId* introuvable.<br/>  |



 

## <a name="remarks"></a>Remarques

La méthode [**newconfig**](inapcomponentconfig3-newconfig.md) doit être utilisée pour allouer des données de configuration pour *configId* avant que cette méthode puisse être appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 






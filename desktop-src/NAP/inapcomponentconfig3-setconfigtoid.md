---
title: Méthode INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Méthode SetConfigToID NAP
- Méthode SetConfigToID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010fdc6cbb236a113e4f1804d3a4780c0e6a72f89b1f03bf90f1d99a92dc2bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781079"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>INapComponentConfig3 :: SetConfigToID, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **SetConfigToID** est implémentée par les validateurs d’intégrité système (SHV) pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configID* \[ dans\]
</dt> <dd>

Valeur qui représente la configuration. *ConfigId* est attribué par le service NPS (Network Policy Server) et est unique dans la SHV. Si *configId* a la valeur 0, la configuration par défaut de l’SHV est définie.

</dd> <dt>

*nombre* \[ dans\]
</dt> <dd>

Taille, en octets, des données de configuration dans les *données*.

</dd> <dt>

*données* \[ dans\]
</dt> <dd>

En entrée, tableau d’octets qui contient les données de configuration définies sur *configId*.

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

 

 






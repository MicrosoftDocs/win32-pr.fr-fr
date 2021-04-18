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
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513045"
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



 

## <a name="remarks"></a>Notes

La méthode [**newconfig**](inapcomponentconfig3-newconfig.md) doit être utilisée pour allouer des données de configuration pour *configId* avant que cette méthode puisse être appelée.

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

 

 






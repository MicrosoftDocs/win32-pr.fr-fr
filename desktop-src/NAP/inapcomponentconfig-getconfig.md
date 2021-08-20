---
title: INapComponentConfig GetConfig, méthode (NapCommon. h)
description: Récupère la configuration du composant du programme de validation d’intégrité système (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Méthode GetConfig NAP
- GetConfig, méthode NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dc5495df10e3a5ff3907941644c5558aea35d29b52c8773fb56314c4a8620c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134497"
---
# <a name="inapcomponentconfiggetconfig-method"></a>INapComponentConfig :: GetConfig, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetConfig** récupère la configuration du composant du programme de validation d’intégrité système (SHV).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCount* \[ à\]
</dt> <dd>

Taille, en octets, de l’objet blob de configuration de *données* .

</dd> <dt>

*données* \[ à\]
</dt> <dd>

Pointeur vers l’adresse des données de configuration du composant SHV.

> [!Note]  
> Les données de configuration exportées à partir d’un ordinateur x86 à l’aide de la méthode **GetConfig** peuvent être importées sur un ordinateur x64 à l’aide de la méthode [**setconfig**](inapcomponentconfig-setconfig.md) , et vice versa. Par conséquent, les données de configuration doivent être dans un format indépendant de l’architecture, tel que XML. L’utilisation de XML au lieu d’un flux d’octets permet d’utiliser plus facilement des données de configuration sur différentes architectures. Les éléments XML utilisés dans les données de configuration sont déterminés par l’implémenteur.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Le paramètre de données doit être alloué par l’appelé (implémenteur de composants) à l’aide de **CoTaskMemAlloc** et libéré par l’appelant à l’aide de **CoTaskMemFree**.

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

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 






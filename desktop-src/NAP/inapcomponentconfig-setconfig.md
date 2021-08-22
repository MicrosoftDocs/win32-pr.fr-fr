---
title: Méthode INapComponentConfig SetConfig (NapCommon. h)
description: Définit la configuration du composant du programme de validation d’intégrité système (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Méthode SetConfig NAP
- Méthode SetConfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode SetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940197"
---
# <a name="inapcomponentconfigsetconfig-method"></a>INapComponentConfig :: SetConfig, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **setconfig** définit la configuration du composant du programme de validation d’intégrité système (SHV).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bCount* \[ dans\]
</dt> <dd>

Taille, en octets, de l’objet blob de configuration de *données* .

</dd> <dt>

*données* \[ dans\]
</dt> <dd>

Pointeur vers les données de configuration du composant SHV.

> [!Note]  
> Les données de configuration exportées à partir d’un ordinateur x86 à l’aide de la méthode [**GetConfig**](inapcomponentconfig-getconfig.md) peuvent être importées sur un ordinateur x64 à l’aide de la méthode **setconfig** , et vice versa. Par conséquent, les données de configuration doivent être dans un format indépendant de l’architecture, tel que XML. L’utilisation de XML au lieu d’un flux d’octets permet d’utiliser plus facilement des données de configuration sur différentes architectures. Les éléments XML utilisés dans les données de configuration sont déterminés par l’implémenteur.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Les informations de contrôle de version des composants doivent être incluses dans l’objet blob de configuration de *données* . Les informations de contrôle de version peuvent être utilisées lors de la migration d’une version de SHV vers une autre.

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

[**INapConponentConfig :: GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 






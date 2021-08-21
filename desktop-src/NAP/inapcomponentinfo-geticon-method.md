---
title: Méthode INapComponentInfo GetIcon (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir l’icône d’un client d’intégrité.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Méthode GetIcon NAP
- Méthode GetIcon NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1711c186d107418d95ccaf19e2a1440b0cecfc0e32fc8c425754d2d9fc19a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134433"
---
# <a name="inapcomponentinfogeticon-method"></a>INapComponentInfo :: GetIcon, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapComponentInfo :: GetIcon** est utilisée par le système NAP pour obtenir l’icône d’un client de contrôle d’intégrité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dllFilePath* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) utilisé pour retourner le chemin d’accès de fichier de la dll qui contient l’icône.

</dd> <dt>

*iconResourceId* \[ à\]
</dt> <dd>

Pointeur vers la valeur utilisée pour retourner l’ID de ressource de l’icône à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Les icônes doivent être localisées en fonction de l’ID de langue du thread appelant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 






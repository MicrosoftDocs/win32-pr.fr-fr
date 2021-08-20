---
title: Méthode ResourceLocator. AddOption (WSManDisp. h)
description: Ajoute les données supplémentaires requises pour traiter la demande. Par exemple, certains fournisseurs WMI peuvent nécessiter un objet IWbemContext ou SWbemNamedValueSet avec des informations spécifiques au fournisseur.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode AddOption
- méthode AddOption Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112964"
---
# <a name="resourcelocatoraddoption-method"></a>Méthode ResourceLocator. AddOption

Ajoute les données supplémentaires requises pour traiter la demande. Par exemple, certains fournisseurs WMI peuvent nécessiter un objet [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) avec des informations spécifiques au fournisseur. Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nomoptist* \[ dans\]
</dt> <dd>

Nom (clé) de l’objet de données facultatif.

</dd> <dt>

*ValeurContrôle* \[ dans\]
</dt> <dd>

Valeur fournie pour l’objet de données facultatif.

</dd> <dt>

*mustComply* \[ dans\]
</dt> <dd>

Indicateur qui indique que l’option doit être traitée. La valeur par défaut est **false** (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

**IWSManResourceLocator :: AddOption** est la méthode C++ correspondante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 


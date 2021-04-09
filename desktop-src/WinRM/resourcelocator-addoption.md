---
title: Méthode ResourceLocator. AddOption (WSManDisp. h)
description: Ajoute les données supplémentaires requises pour traiter la demande. Par exemple, certains fournisseurs WMI peuvent nécessiter un objet IWbemContext ou SWbemNamedValueSet avec des informations spécifiques au fournisseur.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode AddOption
- Méthode AddOption Windows Remote Management, objet ResourceLocator
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
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032509"
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

## <a name="remarks"></a>Notes

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

 


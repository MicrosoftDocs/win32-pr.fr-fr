---
title: Méthode INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Recherche l’emplacement (index) de l’attribut suivant du type indiqué par SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Méthode FindNextAttribute NAP
- Méthode FindNextAttribute NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, méthode FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4425707487994904d1bd2a622cd1ab66f286469c93e80a8eb01e71c0319426ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939576"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>INapSoHProcessor :: FindNextAttribute, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHProcessor :: FindNextAttribute** recherche l’emplacement (index) de l’attribut suivant du type indiqué par *SoHAttributeType*.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fromLocation* \[ dans\]
</dt> <dd>

Emplacement de départ (index) dans le paquet de déclaration d’intégrité (SoH) à partir duquel commencer la recherche d’attribut. Cette valeur doit être comprise entre 0 et (**numAttrib** -1) où **numAttrib** est récupéré à l’aide de [**INapSoHProcessor :: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> Le paquet SoH utilise des index d’attributs basés sur 0.

 

</dd> <dt>

*type* \[ dans\]
</dt> <dd>

Structure [**SoHAttributeType**](sohattributetype-enum.md) qui contient le type d’attribut à rechercher.

</dd> <dt>

*attributeLocation* \[ à\]
</dt> <dd>

Pointeur qui contient l’emplacement (index) dans le paquet SoH du premier attribut de type *SoHAttributeType* à partir de l’index *fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_fichier d' \_ erreur \_ introuvable**</dt> </dl> | Attribut introuvable.<br/>                                    |



 

## <a name="remarks"></a>Remarques

La méthode **FindNextAttribute** recherche les attributs de type *SoHAttributeType* à partir de l’index spécifié par *fromLocation* et une valeur supérieure jusqu’à ce qu’une correspondance soit trouvée. Si aucune correspondance n’est trouvée, le **fichier d’erreur \_ \_ \_ introuvable** est retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 






---
title: Propriété ITsSbEnvironment Name
description: Récupère une valeur qui indique le nom de l’environnement qui héberge l’ordinateur cible.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Propriété Name Services Bureau à distance
- Name, propriété Services Bureau à distance, ITsSbEnvironment, interface
- Services Bureau à distance de l’interface ITsSbEnvironment, propriété Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072199"
---
# <a name="itssbenvironmentname-property"></a>ITsSbEnvironment :: Name, propriété

Récupère une valeur qui indique le nom de l’environnement qui héberge l’ordinateur cible.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une variable **BSTR** qui contient le nom de l’environnement.

## <a name="remarks"></a>Remarques

Cette méthode retourne une chaîne qui n’est pas utilisée directement par Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance). Le Service Broker pour les connexions Bureau à distance transmet cette chaîne aux plug-ins de ressources.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| MIDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 






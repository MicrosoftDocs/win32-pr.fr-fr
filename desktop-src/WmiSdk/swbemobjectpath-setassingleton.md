---
description: La méthode SetAsSingleton de l’objet SWbemObjectPath force le chemin d’accès à l’adresse d’une instance WMI Singleton d’une classe. Une classe singleton est une classe qui ne peut jamais avoir plus d’une instance.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Méthode SWbemObjectPath. SetAsSingleton (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918696"
---
# <a name="swbemobjectpathsetassingleton-method"></a>Méthode SWbemObjectPath. SetAsSingleton

La méthode **SetAsSingleton** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) force le chemin d’accès à l’adresse d’une instance WMI Singleton d’une classe. Une classe singleton est une classe qui ne peut jamais avoir plus d’une instance.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md). SWbemObjectPath

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **SetAsSingleton** , l’objet **Err** peut contenir le code d’erreur ci-dessous.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 





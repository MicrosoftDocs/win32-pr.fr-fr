---
description: La méthode SetAlias configure un alias H. 323 par défaut pour l’adresse. Cet alias sera utilisé dans le programme d’installation d’un appel H. 323 afin que l’autre partie sache le nom de ce tiers.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx :: SetAlias, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532979"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx :: SetAlias, méthode

\[**SetAlias** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetAlias** configure un alias H. 323 par défaut pour l’adresse. Cet alias sera utilisé dans le programme d’installation d’un appel H. 323 afin que l’autre partie sache le nom de ce tiers.

L’appel de cette méthode une deuxième fois remplace l’alias précédent.

L’alias défini sur cette interface est utilisé uniquement lorsqu’il n’existe aucun autre moyen pour le TSP de trouver un alias approprié. À l’avenir, lorsque la prise en charge de Gatekeeper sera ajoutée au TSP, l’alias inscrit auprès de l’opérateur de l’opérateur ou attribué par l’opérateur de l’opérateur remplacera ce qui est défini par cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strAlias* \[ dans\]
</dt> <dd>

Alias à utiliser, en Unicode. La terminaison **null** n’est pas obligatoire.

</dd> <dt>

*dwLength* \[ dans\]
</dt> <dd>

Longueur du nom d’alias en nombre de caractères, y compris la marque de fin **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                               | Description                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | La méthode a réussi.<br/>                                                                                                     |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le nombre de caractères indiqué dans *dwLength* dépasse le nombre réel de caractères dans le paramètre *strAlias* .<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 





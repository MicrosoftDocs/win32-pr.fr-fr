---
description: 'IEnumMedia :: Next, méthode-la méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia :: Next, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c526ce608066f8b3e67affb10bd777042d0d2e93cf02887ba5bfd49a744e931a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865929"
---
# <a name="ienummedianext-method"></a>IEnumMedia :: Next, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d’éléments demandés.

</dd> <dt>

*pval* \[ à\]
</dt> <dd>

Pointeur vers l’interface [**ITMedia**](itmedia.md) .

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Pointeur vers le nombre d’éléments réellement fournis. Peut avoir la **valeur null** si *celt* est un.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                     | Signification                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | La méthode a retourné la valeur *celt* Number of Elements.<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | Le nombre d’éléments restants était inférieur à *celt*.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *pval* n’est pas un pointeur valide.<br/>       |



 

## <a name="remarks"></a>Remarques

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMedia**](itmedia.md) retournée par **IEnumMedia :: Next**. L’application doit appeler **Release** sur l’interface **ITMedia** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 





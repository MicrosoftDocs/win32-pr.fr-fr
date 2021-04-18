---
description: La méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération. Cette méthode est masquée dans les Visual Basic et les langages de script.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant :: Next, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533471"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant :: Next, méthode

\[**Ensuite** , il n’est pas possible de l’utiliser dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération. Cette méthode est masquée dans les Visual Basic et les langages de script.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d’éléments demandés.

</dd> <dt>

*ppElements* \[ à\]
</dt> <dd>

Pointeur vers des interfaces [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Pointeur vers le nombre d’éléments réellement fournis. Peut avoir la **valeur null** si *celt* est un.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a retourné la valeur *celt* Number of Elements.<br/>           |
| <dl> <dt>**S \_ false**</dt> </dl>       | Le nombre d’éléments restants était inférieur à *celt*.<br/>   |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppElements* n’est pas un pointeur valide.<br/>   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

L’interface TAPI appelle la méthode [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur l’interface [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) retournée par **IEnumParticipant :: Next**. L’application doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur l’interface **ITAgentHandler** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 


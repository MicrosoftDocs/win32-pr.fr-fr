---
description: La méthode Clone crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel. Cette méthode est masquée dans les Visual Basic et les langages de script.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant :: Clone, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534894"
---
# <a name="ienumparticipantclone-method"></a>IEnumParticipant :: Clone, méthode

\[Le **clone** ne peut pas être utilisé dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel. Cette méthode est masquée dans les Visual Basic et les langages de script.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* \[ à\]
</dt> <dd>

Pointeur vers une nouvelle interface [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppEnum* n’est pas un pointeur valide.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>  | A échoué pour des raisons inconnues.<br/>                          |



 

## <a name="remarks"></a>Notes

L’interface TAPI appelle la méthode [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sur l’interface [**IEnumParticipant**](ienumparticipant.md) retournée par **IEnumParticipant :: Clone**. L’application doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur l’interface **IEnumParticipant** pour libérer les ressources qui lui sont associées.

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

 


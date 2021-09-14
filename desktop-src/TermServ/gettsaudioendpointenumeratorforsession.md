---
title: GetTSAudioEndpointEnumeratorForSession fonction de rappel
description: Retourne une référence à un énumérateur de point de terminaison audio pour l’ID de session spécifié.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction de rappel GetTSAudioEndpointEnumeratorForSession
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324673"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>GetTSAudioEndpointEnumeratorForSession fonction de rappel

Retourne une référence à un énumérateur de point de terminaison audio pour l’ID de session spécifié. Les consommateurs de cet énumérateur de point de terminaison audio, tels que MMDevAPI.dll, appellent cette fonction pour récupérer un énumérateur de point de terminaison audio dans une session Services Bureau à distance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SessionID* \[ dans\]
</dt> <dd>

Identificateur de la session de Services Bureau à distance.

</dd> <dt>

*ppEndpointEnumerator* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers une interface [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne la valeur **\_ OK**.

## <a name="remarks"></a>Notes

Cette fonction n’est pas définie dans un fichier d’en-tête. Vous devez implémenter et exporter cette fonction dans votre énumérateur de point de terminaison personnalisé et utiliser la signature indiquée dans le bloc de syntaxe plus haut dans cette rubrique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>         |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Implémentation d’un énumérateur de point de terminaison audio personnalisé](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 


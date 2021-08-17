---
title: MpErrorMessageFormat, fonction (MpClient. h)
description: Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 124bf9e2c5c2ecc18f286b99f0c3b93695abd3f6a40853fcc47de580edef5db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883506"
---
# <a name="mperrormessageformat-function"></a>MpErrorMessageFormat fonction)

Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*hrError* \[ dans\]
</dt> <dd>

Type : **HRESULT**

Code d’erreur basé sur **HRESULT**.

</dd> <dt>

*pwszErrorDesc* \[ à\]
</dt> <dd>

Type : **LPWStr \***

Retourne un message d’erreur mis en forme basé sur *hrError*. Cette chaîne doit être libérée à l’aide de [**MpFreeMemory**](mpfreememory.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.

## <a name="remarks"></a>Remarques

Cette fonction est en charge de la mise en forme des codes d’erreur système en plus des codes d’erreur spécifiques retournés par les fonctions de protection contre les programmes malveillants. Les codes d’erreur **HRESULT** spécifiques aux fonctions de protection contre les programmes malveillants ont une fonctionnalité de 0x50. Voici une liste d’un sous-ensemble de codes d’erreur spécifiques à la protection contre les programmes malveillants qui peuvent être renvoyés par différentes fonctions de protection contre les programmes malveillants. À l’aide **de la macro HRESULT \_ de l' \_ \_ État MP**, les codes d’erreur suivants peuvent être convertis en **HRESULT**. Voir aussi [codes d’erreur du moteur anti-programme malveillant Forefront Client Security](https://support.microsoft.com/kb/939359) pour obtenir la liste des autres codes d’erreur possibles.



| Code d'erreur                              | Description                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ MP \_ noengine                     | Aucun moteur n’est chargé dans le service anti-programme malveillant pour effectuer l’opération demandée.                                              |
| ERREUR \_ MP- \_ aucune \_ mémoire                   | Le moteur du logiciel anti-programme malveillant a rencontré une situation sans mémoire.                                                               |
| ERREUR \_ échec de la suppression du pack d' \_ installation \_               | Échec de l’opération de suppression pour une menace spécifique.                                                                              |
| échec de la mise en quarantaine du pack d’erreur \_ \_ \_           | Échec de l’opération de mise en quarantaine pour une menace spécifique.                                                                          |
| ERREUR \_ MP \_ Threat \_ \_ introuvable           | La menace spécifique n’existe plus dans le système.                                                                         |
| ERREUR de \_ suppression du pack d' \_ installation \_ non \_ prise en charge       | La suppression de l’opération pour une menace spécifique à l’intérieur du type de conteneur n’est pas prise en charge.                                          |
| ERREUR \_ MP de \_ suppression du \_ \_ conteneur immuable | En raison de la stratégie du moteur, une opération de suppression d’une menace spécifique à l’intérieur d’un conteneur bloqué n’est pas prise en charge. (Archives de messagerie.) |
| ERREUR \_ MP \_ BADDB \_ OLDENGINE             | La demande de mise à jour de signature a fourni un moteur ou des fichiers de signature plus anciens.                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Codes d’erreur du moteur anti-programme malveillant Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 






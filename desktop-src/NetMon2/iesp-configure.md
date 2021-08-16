---
description: La méthode Configure envoie les informations de configuration d’une capture.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5ae0fba6885db46d987e59517cdc30dab484974869c67c85a257044e5eec58b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365668"
---
# <a name="iespconfigure-method"></a>IESP :: configure, méthode

La méthode **configure** envoie les informations de configuration d’une capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConfigurationBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB configuré par l’appelant.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur. Pour plus d’informations sur le contenu d’un objet BLOB d’erreur, consultez la section Notes de cette rubrique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                         | Description                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>                | Le NPP n’est pas connecté au réseau.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>                      | le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connecter](iesp-connect.md) .<br/>                                                                                                         |
| <dl> <dt>**\_capture NMERR**</dt> </dl>                     | Le NPP signale que la session de capture a démarré.<br/>                                                                                                                                                  |
| <dl> <dt>**\_déclencheur NMERR non conforme \_**</dt> </dl>              | La partie déclencheur de l’objet BLOB de configuration est endommagée.<br/>                                                                                                                                              |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt> </dl> | Une entrée nécessaire à l’exécution de cette opération est manquante dans l’objet BLOB de configuration spécifié par *hConfigurationBlob* . Examinez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer quelle entrée est introuvable.<br/> |
| <dl> <dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt> </dl>       | L’objet BLOB est endommagé.<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt> </dl>        | La méthode **CreateBlob** n’a pas été appelée.<br/>                                                                                                                                                         |
| <dl> <dt>**NMERR \_ \_ objet blob non valide**</dt> </dl>                 | L’objet pointé n’est pas un objet BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt> </dl>         | La chaîne ne se termine pas par un caractère null.<br/>                                                                                                                                                                     |
| <dl> <dt>**NMERR \_ objet blob de niveau supérieur \_**</dt> </dl>                 | Le numéro de version de l’objet BLOB est incorrect.<br/>                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl>               | Aucune mémoire n’était disponible. Arrêtez Windows pour libérer des ressources.<br/>                                                                                                                                       |
| <dl> <dt>**\_délai d’expiration de NMERR**</dt> </dl>                       | Le délai d'attente de la requête a expiré.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Remarques

Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré et arrêté, mais qui n’est pas déconnecté.

L’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*. L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 





---
description: La méthode Configure envoie les informations de configuration utilisées pour une capture.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Méthode IDelaydCConfigure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484313"
---
# <a name="idelaydcconfigure-method"></a>IDelaydC :: configure, méthode

La méthode **configure** envoie les informations de configuration utilisées pour une capture.

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

Handle vers l’objet BLOB qui contient les informations de configuration.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur. Pour plus d’informations sur le contenu d’un objet BLOB d’erreur, consultez la section Notes de cette rubrique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                      | Description                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR**</dt> </dl>                  | Le NPP signale que la session de capture a démarré.<br/>                          |
| <dl> <dt>**\_disque NMERR \_ non \_ local \_ fixe**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ n’a \_ pas pu \_ créer de \_ mémoire**</dt> </dl> |                                                                                           |
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl>            | Aucune mémoire n’était disponible. Arrêtez Windows pour libérer des ressources.<br/>               |
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl>         | L’objet BLOB de configuration spécifié par le paramètre hConfiguration n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté, mais pas déconnecté.

L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*. L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC :: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC :: Stop](idelaydc-stop.md)
</dt> </dl>

 

 





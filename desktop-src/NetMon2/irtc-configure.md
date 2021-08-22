---
description: Envoie des données de configuration pour une capture de données.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'IRTC :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f70674d8e570a2640fe301179b21a9f48ec612a17de69e43bdf5c38db4e65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063909"
---
# <a name="irtcconfigure-method"></a>IRTC :: configure, méthode

La méthode [**configure**](configure.md) envoie les données de configuration d’une capture de données.

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

Handle vers l’objet BLOB configuré par l’appelant.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle d’un objet BLOB d’erreur qui contient des données d’erreur supplémentaires.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                         | Description                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt> </dl>        | La méthode **CreateBlob** n’a pas été appelée.<br/>                                                                                                                                                 |
| <dl> <dt>**NMERR \_ \_ objet blob non valide**</dt> </dl>                 | L’objet pointé n’est pas un objet BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR \_ objet blob de niveau supérieur \_**</dt> </dl>                 | Le numéro de version de l’objet BLOB est incorrect.<br/>                                                                                                                                                          |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ \_ existe déjà**</dt> </dl>  | Objet BLOB dupliqué.<br/>                                                                                                                                                                                |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt> </dl> | L’objet BLOB de configuration spécifié par *hConfigurationBlob* n’a pas d’entrée nécessaire pour effectuer cette opération. Affichez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer l’entrée qui est introuvable.<br/> |
| <dl> <dt>**NMERR \_ , \_ spécificateur ambigu**</dt> </dl>          | Le propriétaire de l’objet BLOB ou les données de catégorie sont manquantes.<br/>                                                                                                                                                    |
| <dl> <dt>**propriétaire de l' \_ objet BLOB NMERR \_ \_ \_ introuvable**</dt> </dl>       | La section propriétaire de l’objet BLOB est introuvable.<br/>                                                                                                                                                          |
| <dl> <dt>**\_catégorie d’objet BLOB NMERR \_ \_ \_ introuvable**</dt> </dl>    | La section de catégorie d’objets BLOB est introuvable.<br/>                                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ catégorie inconnue**</dt> </dl>             | La section de catégorie BLOB a été trouvée, mais n’est pas comprise.<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ balise inconnue**</dt> </dl>                  | La section de la balise BLOB a été trouvée, mais n’est pas comprise.<br/>                                                                                                                                            |
| <dl> <dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt> </dl>       | L’objet BLOB est endommagé.<br/>                                                                                                                                                                           |
| <dl> <dt>**\_déclencheur NMERR non conforme \_**</dt> </dl>              | La partie du déclencheur de l’objet BLOB est endommagée.<br/>                                                                                                                                                    |
| <dl> <dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt> </dl>         | La chaîne ne se termine pas par un caractère null.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Remarques

Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté, mais pas déconnecté.

L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans *hConfigurationBlob*. L’objet BLOB d’erreurs renvoyé contient des données d’erreur que l’application peut utiliser pour la résolution des problèmes. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC :: Connecter](irtc-connect.md)
</dt> <dt>

[OBJETS BLOB Moniteur réseau](network-monitor-blobs.md)
</dt> </dl>

 

 





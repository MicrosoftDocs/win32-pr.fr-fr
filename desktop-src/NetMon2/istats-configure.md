---
description: La méthode Configure envoie les informations de configuration de capture.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStats :: configure, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210047"
---
# <a name="istatsconfigure-method"></a>IStats :: configure, méthode

La méthode **configure** envoie les informations de configuration de capture.

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

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                         | Description                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt> </dl>         | La chaîne ne se termine pas par un caractère null.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt> </dl>        | La méthode **CreateBlob** n’a pas été appelée.<br/>                                                                                                                                                                                |
| <dl> <dt>**NMERR \_ \_ objet blob non valide**</dt> </dl>                 | L’objet pointé n’est pas un objet BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ objet blob de niveau supérieur \_**</dt> </dl>                 | Le numéro de version de l’objet BLOB est incorrect.<br/>                                                                                                                                                                                         |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ \_ existe déjà**</dt> </dl>  | Une entrée d’objet BLOB existe déjà.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt> </dl> | L’objet BLOB de configuration spécifié par le paramètre *hConfigurationBlob* n’a pas d’entrée nécessaire pour effectuer cette opération. Examinez l’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* pour déterminer quelle entrée est introuvable.<br/> |
| <dl> <dt>**NMERR \_ , \_ spécificateur ambigu**</dt> </dl>          | L’objet BLOB n’a pas d’informations de propriétaire ou de catégorie.<br/>                                                                                                                                                                                 |
| <dl> <dt>**propriétaire de l' \_ objet BLOB NMERR \_ \_ \_ introuvable**</dt> </dl>       | La section propriétaire de l’objet BLOB est introuvable.<br/>                                                                                                                                                                                  |
| <dl> <dt>**\_catégorie d’objet BLOB NMERR \_ \_ \_ introuvable**</dt> </dl>    | La section de catégorie de l’objet BLOB est introuvable.<br/>                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ \_ catégorie inconnue**</dt> </dl>             | Les informations de catégorie ont été trouvées, mais elles ne sont pas comprises.<br/>                                                                                                                                                                            |
| <dl> <dt>**NMERR \_ \_ balise inconnue**</dt> </dl>                  | Les informations de balise ont été trouvées mais ne sont pas comprises.<br/>                                                                                                                                                                                 |
| <dl> <dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt> </dl>       | L’objet BLOB est endommagé.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_déclencheur NMERR non conforme \_**</dt> </dl>              | La partie du déclencheur de l’objet BLOB est endommagée.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

Vous devez appliquer cette méthode pour redémarrer un NPP qui a été démarré, arrêté mais non déconnecté.

L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob de configuration spécifié dans le paramètre *hConfigurationBlob* . L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[ISTATS :: Connect](istats-connect.md)
</dt> <dt>

[OBJETS BLOB Moniteur réseau](network-monitor-blobs.md)
</dt> </dl>

 

 





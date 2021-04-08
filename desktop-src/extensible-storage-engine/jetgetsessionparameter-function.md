---
description: 'En savoir plus sur : fonction JetGetSessionParameter'
title: JetGetSessionParameter fonction)
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0ac02142d48009d668d903b39163b425d738b55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861933"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter fonction)


_**S’applique à :** Windows | Serveur Windows_

La fonction **JetGetSessionParameter** lit le paramètre de session pour la session donnée.

La fonction **JetGetSessionParameter** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.

*sesparamid*

ID du paramètre de session à définir.

*pvParam*

Données dans ce paramètre de session.

*cbParamMax*

Taille maximale du jeu de données dans ce paramètre de session.

*pcbParamActual*

Taille réelle du jeu de données dans ce paramètre de session.

### <a name="return-value"></a>Valeur retournée

En cas de réussite, la mémoire tampon de sortie appropriée pour le paramètre de session demandé sera définie sur la valeur de ce paramètre de session.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.

#### <a name="remarks"></a>Notes

Le paramètre de session est utilisé pour la durée de vie de la session ou jusqu’à ce que la valeur soit réinitialisée.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)

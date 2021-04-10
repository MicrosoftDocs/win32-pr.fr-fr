---
description: 'En savoir plus sur : paramètres de rappel'
title: Paramètres de rappel
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e06ed65bbeae195060e4de10424a76a4228f20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114095"
---
# <a name="callback-parameters"></a>Paramètres de rappel


_**S’applique à :** Windows | Serveur Windows_

## <a name="callback-parameters"></a>Paramètres de rappel

Cette rubrique contient des paramètres qui sont utilisés pour les rappels.

*JET_paramDisableCallbacks*  
65  

Ce paramètre désactive tous les rappels du moteur de base de données pour les fonctions fournies par l’application. Elle est principalement destinée à prendre en charge les utilitaires du moteur de base de données et n’est pas destinée à être utilisée dans votre application.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramEnablePersistedCallbacks*  
156  

Ce paramètre permet l’utilisation de rappels persistants dans la base de données. Dans les versions antérieures à Windows Vista, l’utilisation de rappels persistants était activée par défaut. Les applications doivent maintenant activer explicitement l’utilisation de rappels persistants au moment de l’exécution à l’aide de ce paramètre. Si ce paramètre n’est pas défini, toute opération de base de données qui requiert l’appel d’un rappel échouera avec JET_errCallbackFailed. Ce paramètre n’affecte pas les rappels spécifiés au moment de l’exécution avec les mécanismes suivants : JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou un paramètre de rappel explicite à une API jet. Il est toujours possible de créer des éléments de schéma qui contiennent des rappels persistants, même si l’utilisation de ces rappels persistants est interdite. Quand ce paramètre est défini sur false, il remplace JET_paramDisableCallbacks.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Faux</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows Vista et versions ultérieures</p></td>
</tr>
</tbody>
</table>


*JET_paramRuntimeCallback*  
73  

Ce paramètre configure le moteur à l’aide d’une fonction de rappel d’exécution qui implémente l’interface [JET_CALLBACK](./jet-callback-callback-function.md) . Ce rappel peut être appelé pour les raisons suivantes : [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md). Pour plus d’informations, consultez [JetSetLS](./jetsetls-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>NULL</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Pointeur de fonction (JET_API_PTR)</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Windows XP et versions ultérieures</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)

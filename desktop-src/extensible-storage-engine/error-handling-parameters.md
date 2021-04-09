---
description: En savoir plus sur les paramètres de gestion des erreurs
title: Paramètres de gestion des erreurs
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb225d7dbb67655286635320352060bcf2cb8a5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868734"
---
# <a name="error-handling-parameters"></a>Paramètres de gestion des erreurs


_**S’applique à :** Windows | Serveur Windows_

## <a name="error-handling-parameters"></a>Paramètres de gestion des erreurs

Cette rubrique contient des paramètres qui sont utilisés pour la gestion des erreurs.

*JET_paramErrorToString* 70  

Ce paramètre peut être utilisé pour convertir un [JET_ERR](./jet-err.md) en chaîne. Cette opération s’effectue à l’aide d’un appel spécial à [JetGetSystemParameter](./jetgetsystemparameter-function.md) où la mémoire tampon de sortie entière contient la valeur [JET_ERR](./jet-err.md) à convertir (en tant que paramètre d’entrée) et la mémoire tampon de sortie de chaîne retourne la chaîne d’erreur correspondante. La chaîne se présente comme suit : « JET_errSuccess, opération réussie ». La chaîne est composée du nom symbolique de la chaîne, d’une virgule, puis d’une description textuelle simple de l’erreur. La chaîne de description peut elle-même contenir des virgules. Si l’erreur n’est pas reconnue, la chaîne sera « erreur inconnue, erreur inconnue ».

**Remarque**  Ce paramètre est en lecture seule.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>Spécial</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Non</p></td>
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
<td><p>Tous</p></td>
</tr>
</tbody>
</table>

*JET_paramExceptionAction*  
98  

Ce paramètre contrôle ce qui se produit lorsqu’une exception est levée par le moteur de base de données ou le code qui est appelé par le moteur de base de données. Quand la valeur JET_ExceptionMsgBox, toute exception est levée dans le filtre d’exception non géré Windows. L’exception est alors gérée en tant qu’échec de l’application. L’objectif est d’empêcher le code d’application d’essayer à tort d’intercepter et d’ignorer une exception générée par le moteur de base de données. Cela ne peut pas être autorisé, car une base de données endommagée peut se produire. Si l’application souhaite gérer correctement ces exceptions, la protection peut être désactivée en définissant ce paramètre sur JET_ExceptionNone.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>JET_ExceptionMsgBox</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>JET_ExceptionMsgBox, JET_ExceptionNone</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :  </strong>  º</p>
<p><strong>Windows Vista :</strong>  Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p><strong>Windows 2000, Windows XP et Windows Server 2003 :  </strong>  º</p>
<p><strong>Windows Vista :</strong>  Oui</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Oui</p></td>
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
<td><p>Tous</p></td>
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
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>

### <a name="see-also"></a>Voir aussi

[Constantes de gestion des erreurs](./error-handling-constants.md)  
[Codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)

---
description: 'En savoir plus sur : structure JET_USERDEFINEDDEFAULT'
title: Structure JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
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
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520756"
---
# <a name="jet_userdefineddefault-structure"></a>Structure JET_USERDEFINEDDEFAULT


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_userdefineddefault-structure"></a>Structure JET_USERDEFINEDDEFAULT

La structure **JET_USERDEFINEDDEFAULT** est spécifiée conjointement avec JET_bitColumnUserDefinedDefault pour attribuer une valeur par défaut à une nouvelle colonne qui est déterminée à l’aide d’un rappel. Cette technique peut être utilisée pour implémenter des colonnes calculées.

**Windows XP :** La structure **JET_USERDEFINEDDEFAULT** est introduite dans Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Membres

**szCallback**

Nom d’exportation de la fonction qui implémente le rappel au format « \! fonction de module ».

Le rappel est conservé dans le cadre du schéma de colonne. L’exécutable hôte et le nom d’exportation réels de la fonction doivent être rendus persistants pour permettre la recherche de l’adresse réelle de la fonction au moment de l’exécution.

Le nom du module est le nom du fichier binaire hôte qui contient la fonction. Le nom de la fonction est le nom de l’exportation pour cette fonction. Ces deux informations seront utilisées par le moteur de base de données au moment de l’exécution pour localiser l’adresse réelle du rappel en exécutant un appel [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sur le nom du module, suivi d’un appel [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) sur le nom de la fonction.

Par exemple, si le rappel a été implémenté dans une DLL nommée MyCallback.DLL et que cette DLL était stockée dans C : \\ MyApplication et que la fonction implémentant le rappel a été exportée à partir de la dll en tant que UserDefinedDefaultCallback, la chaîne requise serait « C : \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback ».

**Remarque**  «» Incorporé \! les caractères de la partie module du nom de rappel ne sont pas pris en charge.

Il est fortement recommandé d’utiliser un nom de rappel qui n’est pas une fonction de l’architecture de l’hôte. Par exemple, n’utilisez pas d’exportations décorées comme stdcall ( UserDefinedDefaultCallback@32 ), car cette Convention d’appel est uniquement prise en charge sur les ordinateurs x86. Si un rappel de ce type a été utilisé, la base de données ne peut être utilisée que sur un ordinateur x86. Dans ce cas, vous devez utiliser un alias pour effectuer une exportation non indépendante de la plateforme.

Il est fortement recommandé d’utiliser le chemin d’accès complet du nom du module qui implémente le rappel. Si un chemin d’accès relatif est utilisé, le processus qui héberge la base de données peut être vulnérable aux attaques par un binaire non autorisé.

L’application doit passer uniquement les rappels approuvés au moteur de base de données. Le moteur de base de données chargera le fichier binaire pour vérifier son existence lors de la création de la colonne associée. Si le chemin d’accès au fichier binaire n’est pas validé ou connu comme approuvé, il peut attaquer le processus qui héberge la base de données.

**pbUserData**

Bloc autonome de données définies par l’utilisateur à passer au rappel lorsqu’il est appelé. Le bloc de données fourni est conservé en tant que partie du schéma de colonne. Par conséquent, le bloc de données doit être entièrement autonome et ne peut pas faire référence à des données qui se trouvent en dehors de la portée de la base de données.

Si **pbUserData** est égal à zéro, la valeur de **cbUserData** est ignorée. Dans ce cas, aucune donnée définie par l’utilisateur n’est passée au rappel lorsqu’il est appelé.

**cbUserData**

Consultez **pbUserData**.

**szDependantColumns**

Réservé pour un usage futur.

Ce membre doit toujours avoir la valeur NULL.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) et <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)

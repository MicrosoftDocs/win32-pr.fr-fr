---
description: 'En savoir plus sur : énumération JET_cbtyp'
title: Énumération JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 209d3ffe9721f51b8c2d510eecb5408ac66cdbeb58309d1f033e2d23730328ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116229"
---
# <a name="jet_cbtyp-enumeration"></a>Énumération JET_cbtyp

Type de progression signalée.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a>Membres

<table>
<thead>
<tr class="header">
<th></th>
<th>Nom du membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Null</td>
<td>Ce rappel est réservé et toujours considéré comme non valide.</td>
</tr>
<tr class="even">
<td></td>
<td>Finalize</td>
<td>Une colonne finalisable est passée à zéro.</td>
</tr>
<tr class="odd">
<td></td>
<td>AvantInsertion</td>
<td>Ce rappel se produit juste avant l’insertion d’un nouvel enregistrement dans une table par un appel à JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>Évènement</td>
<td>Ce rappel se produit juste après l’insertion d’un nouvel enregistrement dans une table par un appel à JetUpdate mais avant le retour de JetUpdate.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Ce rappel se produit juste avant un enregistrement existant dans une table en cours de modification par un appel à JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Ce rappel se produit juste après qu’un enregistrement existant dans une table a été modifié par un appel à JetUpdate mais avant le retour de JetUpdate.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Ce rappel se produit juste avant qu’un enregistrement existant dans une table ne soit supprimé par un appel à JetDelete.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Ce rappel se produit juste après la suppression d’un enregistrement existant dans une table par un appel à JetDelete.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Ce rappel se produit lorsque le moteur doit récupérer la valeur par défaut définie par l’utilisateur d’une colonne à partir de l’application. Ce rappel est essentiellement une implémentation limitée de JetRetrieveColumn qui est évaluée par l’application. Un maximum de valeur de colonne peut être retourné pour une valeur par défaut définie par l’utilisateur.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Ce rappel se produit lorsque la défragmentation en ligne d’une base de données telle qu’elle est lancée par JetDefragment s’est arrêtée en raison de l’exécution du processus ou de la limite de temps atteinte.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>ce rappel se produit lorsque l’application doit nettoyer le handle de contexte pour l’Stockage Local associée à un curseur libéré par le moteur de base de données. Pour plus d’informations, consultez JetSetLS. Le délégué pour cette raison de rappel est configuré au moyen de JetSetSystemParameter avec JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>ce rappel se produit en raison de la nécessité pour l’application de nettoyer le descripteur de contexte pour le Stockage Local associé à une table qui est libérée par le moteur de base de données. Pour plus d’informations, consultez JetSetLS. Le délégué pour cette raison de rappel est configuré au moyen de JetSetSystemParameter avec JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

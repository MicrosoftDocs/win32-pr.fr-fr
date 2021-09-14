---
description: 'En savoir plus sur : énumération OpenTableGrbit'
title: Énumération OpenTableGrbit
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854104"
---
# <a name="opentablegrbit-enumeration"></a>Énumération OpenTableGrbit

Options pour JetOpenTable.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>None</td>
<td>Options par défaut.</td>
</tr>
<tr class="even">
<td></td>
<td>DenyWrite</td>
<td>Cette table ne peut pas être ouverte pour un accès en écriture par une autre session.</td>
</tr>
<tr class="odd">
<td></td>
<td>DenyRead</td>
<td>Cette table ne peut pas être ouverte pour un accès en lecture par une autre session.</td>
</tr>
<tr class="even">
<td></td>
<td>Lecture seule</td>
<td>Demandez un accès en lecture seule à la table.</td>
</tr>
<tr class="odd">
<td></td>
<td>Peut être mise à jour</td>
<td>Demandez l’accès en écriture à la table.</td>
</tr>
<tr class="even">
<td></td>
<td>PermitDDL</td>
<td>Autorisez les modifications DDL dans une table marquée comme FixedDDL. Cette option doit être utilisée avec DenyRead.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>Ne pas mettre en cache les pages pour cette table.</td>
</tr>
<tr class="even">
<td></td>
<td>Prélecture</td>
<td>Indique que la table n’est probablement pas dans le cache des tampons, et que la prélecture peut être bénéfique pour les performances.</td>
</tr>
<tr class="odd">
<td></td>
<td>Séquentiel</td>
<td>Supposons un modèle d’accès séquentiel et des pages de base de données de prérécupération.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>La table appartient à la classe de statistiques 1.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>La table appartient à la classe de statistiques 2.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>La table appartient à la classe stats 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>La table appartient à la classe stats 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>La table appartient à la classe stats 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>La table appartient à la classe stats 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>La table appartient à la classe stats 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>La table appartient à la classe de statistiques 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>La table appartient à la classe stats 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>La table appartient à la classe stats 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>La table appartient à la classe stats 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>La table appartient à la classe de statistiques 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>La table appartient à la classe stats 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>La table appartient à la classe stats 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>La table appartient à la classe stats 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

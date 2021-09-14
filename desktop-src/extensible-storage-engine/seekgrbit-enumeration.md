---
description: 'En savoir plus sur : énumération SeekGrbit'
title: Énumération SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854085"
---
# <a name="seekgrbit-enumeration"></a>Énumération SeekGrbit

Options pour JetSeek.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui correspond exactement à la clé de recherche.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure à une entrée d’index qui correspond exactement aux critères de recherche.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure à une entrée d’index qui correspond exactement aux critères de recherche.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Une plage d’index sera automatiquement configurée pour toutes les clés qui correspondent exactement à la clé de recherche.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

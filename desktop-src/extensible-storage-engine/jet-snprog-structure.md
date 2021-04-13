---
description: 'En savoir plus sur : structure JET_SNPROG'
title: Structure JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
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
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484265"
---
# <a name="jet_snprog-structure"></a>Structure JET_SNPROG


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_snprog-structure"></a>Structure JET_SNPROG

La structure **JET_SNPROG** contient des informations sur la progression d’une opération de longue durée. Lorsque la fonction de rappel est appelée pour notifier l’état de l’opération et que l’opération est toujours en cours, le dernier paramètre de la fonction de rappel est un pointeur vers une structure de **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure **JET_SNPROG** , en octets. Cette valeur confirme la présence des champs suivants.

**cunitDone**

Nombre d’unités de travail déjà terminées pendant la fonction de longue durée.

**cunitTotal**

Nombre d’unités de travail qui doivent être terminées. Cette valeur doit toujours être supérieure ou égale à **cunitDone**.

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


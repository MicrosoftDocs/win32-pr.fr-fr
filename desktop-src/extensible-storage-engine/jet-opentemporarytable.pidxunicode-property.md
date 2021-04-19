---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. pidxunicode'
title: JET_OPENTEMPORARYTABLE. pidxunicode, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520757"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>JET_OPENTEMPORARYTABLE. pidxunicode, propriété

Obtient ou définit les indicateurs de normalisation et l’ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire. Lorsque ce paramètre a la valeur null, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire. Le LCID par défaut est le paramètre régional anglais (États-Unis). Lorsque ce paramètre a la valeur null, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire. Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Membres JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

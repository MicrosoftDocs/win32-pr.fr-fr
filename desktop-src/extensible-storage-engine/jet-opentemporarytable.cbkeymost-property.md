---
description: 'En savoir plus sur : propriété JET_OPENTEMPORARYTABLE. cbKeyMost'
title: JET_OPENTEMPORARYTABLE. cbKeyMost, propriété (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534118"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE. cbKeyMost, propriété

Obtient ou définit la taille maximale d’une clé représentant une ligne donnée. La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées. La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes. Si ce paramètre a la valeur 0 ou 255, la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003. Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données pour l’instance [DatabasePageSize](./jet-param-enumeration.md). Pour [plus](./vistaparam.keymost-field.md) d’informations, consultez.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Membres JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)

---
description: 'En savoir plus sur : JET_INSTANCE. ToString, méthode (String, IFormatProvider)'
title: JET_INSTANCE. ToString, méthode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39511283
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4030a86ed867a2463346dca549acb35809264c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524337"
---
# <a name="jet_instancetostring-method-string-iformatprovider"></a>JET_INSTANCE. ToString, méthode (String, IFormatProvider)

Met en forme la valeur de l’instance actuelle en utilisant le format spécifié.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_INSTANCE
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Paramètres

  - format  
    Type : [System. String](/dotnet/api/system.string)  
    
    [Chaîne](/dotnet/api/system.string) spécifiant le format à utiliser ; ou valeur null pour utiliser le format par défaut défini pour le type de l’implémentation de [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - formatProvider  
    Type : [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider](/dotnet/api/system.iformatprovider) à utiliser pour mettre en forme la valeur ; ou, NULL pour obtenir les informations de format numérique à partir des paramètres régionaux actuels du système d’exploitation.

#### <a name="return-value"></a>Valeur retournée

Type : [System. String](/dotnet/api/system.string)  
[Chaîne](/dotnet/api/system.string) contenant la valeur de l’instance actuelle au format spécifié.  

#### <a name="implements"></a>Implémente

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_INSTANCE](./jet-instance-structure.md)

[Membres JET_INSTANCE](./jet-instance-members.md)

[ToString, surcharge](./jet-instance.tostring-method2.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'En savoir plus sur : JET_HANDLE. ToString, méthode (String, IFormatProvider)'
title: JET_HANDLE. ToString, méthode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.tostring(v=EXCHG.10)
ms:contentKeyID: 39515173
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f807f13bedb879377449cd494cd245b3ad1073488597190866a190b3253f9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039167"
---
# <a name="jet_handletostring-method-string-iformatprovider"></a>JET_HANDLE. ToString, méthode (String, IFormatProvider)

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
Dim instance As JET_HANDLE
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
    
    [Chaîne](/dotnet/api/system.string) spécifiant le format à utiliser. -ou-null pour utiliser le format par défaut défini pour le type de l’implémentation de [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - formatProvider  
    Type : [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider](/dotnet/api/system.iformatprovider) à utiliser pour mettre en forme la valeur. -ou-null pour obtenir les informations de format numérique à partir des paramètres régionaux actuels du système d’exploitation.

#### <a name="return-value"></a>Valeur retournée

Type : [System. String](/dotnet/api/system.string)  
[Chaîne](/dotnet/api/system.string) contenant la valeur de l’instance actuelle au format spécifié.  

#### <a name="implements"></a>Implémente

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_HANDLE](./jet-handle-structure.md)

[Membres JET_HANDLE](./jet-handle-members.md)

[ToString, surcharge](./jet-handle.tostring-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

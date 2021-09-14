---
description: 'En savoir plus sur : classe EsentInvalidFilenameException'
title: EsentInvalidFilenameException, classe
TOCTitle: EsentInvalidFilenameException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidfilenameexception(v=EXCHG.10)
ms:contentKeyID: 55101955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 209347096064d61f9f31fac8ae0552f36fbc9109
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917872"
---
# <a name="esentinvalidfilenameexception-class"></a>EsentInvalidFilenameException, classe

Classe de base pour JET_err. Exceptions InvalidFilename.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentInvalidFilenameException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidFilenameException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidFilenameException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidFilenameException : EsentObsoleteException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentInvalidFilenameException](./esentinvalidfilenameexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

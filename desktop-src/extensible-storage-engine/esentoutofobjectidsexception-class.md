---
description: 'En savoir plus sur : classe EsentOutOfObjectIDsException'
title: EsentOutOfObjectIDsException, classe
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520102"
---
# <a name="esentoutofobjectidsexception-class"></a>EsentOutOfObjectIDsException, classe

Classe de base pour JET_err. Exceptions OutOfObjectIDs.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentFragmentationException](./esentfragmentationexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentOutOfObjectIDsException](./esentoutofobjectidsexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

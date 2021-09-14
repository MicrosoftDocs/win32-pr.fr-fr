---
description: 'En savoir plus sur : classe EsentLogSequenceEndException'
title: EsentLogSequenceEndException, classe
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78de803d31d8e97f9493d605d688916501edba6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007897"
---
# <a name="esentlogsequenceendexception-class"></a>EsentLogSequenceEndException, classe

Classe de base pour JET_err. Exceptions LogSequenceEnd.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentFragmentationException](./esentfragmentationexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentLogSequenceEndException](./esentlogsequenceendexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

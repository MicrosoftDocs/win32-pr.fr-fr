---
description: 'En savoir plus sur : classe EsentFragmentationException'
title: EsentFragmentationException, classe
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106520221"
---
# <a name="esentfragmentationexception-class"></a>EsentFragmentationException, classe

Classe de base pour les exceptions de fragmentation.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentFragmentationException  
            

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentFragmentationException](./esentfragmentationexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Types dérivés

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentFragmentationException  
            [Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchException](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException](./esentlogsequenceendexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfDbtimeValuesException](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException](./esentoutofobjectidsexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException](./esentoutofsequentialindexvaluesexception-class.md)
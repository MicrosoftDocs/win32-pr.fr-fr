---
description: 'En savoir plus sur : classe EsentSessionContextNotSetByThisThreadException'
title: EsentSessionContextNotSetByThisThreadException, classe
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64339a51d0c2afe917ff1fbd41cab996ac0765bf24e2b4b6ae97e98d366f3a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039957"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a>EsentSessionContextNotSetByThisThreadException, classe

Classe de base pour JET_err. Exceptions SessionContextNotSetByThisThread.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentSessionContextNotSetByThisThreadException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentSessionContextNotSetByThisThreadException](./esentsessioncontextnotsetbythisthreadexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

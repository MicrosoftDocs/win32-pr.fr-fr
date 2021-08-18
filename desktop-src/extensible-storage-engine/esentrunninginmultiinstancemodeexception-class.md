---
description: 'En savoir plus sur : classe EsentRunningInMultiInstanceModeException'
title: EsentRunningInMultiInstanceModeException, classe
TOCTitle: EsentRunningInMultiInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginmultiinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3183b3ec68ae86874d8b450a55c236f6787f009ba850c66a5090e87d8d429f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118981829"
---
# <a name="esentrunninginmultiinstancemodeexception-class"></a>EsentRunningInMultiInstanceModeException, classe

Classe de base pour JET_err. Exceptions RunningInMultiInstanceMode.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentRunningInMultiInstanceModeException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInMultiInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInMultiInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInMultiInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentRunningInMultiInstanceModeException](./esentrunninginmultiinstancemodeexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'En savoir plus sur : EsentErrorException. GetObjectData, méthode'
title: EsentErrorException. GetObjectData, méthode
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ff4588429d5b45690763c3f4eefd3553f88f480
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476655"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a>EsentErrorException. GetObjectData, méthode

En cas de substitution dans une classe dérivée, définit [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) avec les informations relatives à l’exception.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Paramètres

  - info  
    Type : [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) qui contient les données d’objet sérialisées concernant l’exception levée.

<!-- end list -->

  - contexte  
    Type : [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    [StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) qui contient des informations contextuelles sur la source ou la destination.

#### <a name="implements"></a>Implémente

[ISerializable. GetObjectData (SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception. GetObjectData (SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>Exceptions


| Exception | Condition | 
|-----------|-----------|
| <a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a> | <p>Le paramètre info est une référence null (Nothing en Visual Basic).</p> | 



## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe EsentErrorException](./esenterrorexception-class.md)

[Membres EsentErrorException](./esenterrorexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'En savoir plus sur : classe EsentPatchFileMissingException'
title: EsentPatchFileMissingException, classe
TOCTitle: EsentPatchFileMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpatchfilemissingexception(v=EXCHG.10)
ms:contentKeyID: 55102469
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edaabc35018c7905542f9a7325efaed300234e66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403436"
---
# <a name="esentpatchfilemissingexception-class"></a>EsentPatchFileMissingException, classe

Classe de base pour JET_err. Exceptions PatchFileMissing.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentPatchFileMissingException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPatchFileMissingException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentPatchFileMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPatchFileMissingException : EsentObsoleteException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentPatchFileMissingException](./esentpatchfilemissingexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'En savoir plus sur : JET_PFNREALLOC délégué'
title: Délégué JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 445cd4084ff187fba0b94e210d587b04660c0fb4dfe9e882e0c5696bfd5392df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730419"
---
# <a name="jet_pfnrealloc-delegate"></a>Délégué JET_PFNREALLOC

Rappel utilisé par JetEnumerateColumns pour allouer de la mémoire pour ses mémoires tampons de sortie.

Cette API n’est pas conforme CLS. 

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Paramètres

  - contexte  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexte donné à JetEnumerateColumns.

<!-- end list -->

  - mémoire  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Si la valeur est différente de zéro, pointeur vers un bloc de mémoire précédemment alloué par ce rappel.

<!-- end list -->

  - requestedSize  
    Type : [System. UInt32](/dotnet/api/system.uint32)  
    
    Nouvelle taille du bloc de mémoire (en octets). Si la valeur est égale à 0 et qu’un bloc de mémoire est spécifié, ce bloc de mémoire est libéré.

#### <a name="return-value"></a>Valeur retournée

Type : [System. IntPtr](/dotnet/api/system.intptr)  
Pointeur vers la mémoire nouvellement allouée. Si la mémoire n’a pas pu être allouée, la [valeur zéro](/dotnet/api/system.intptr.zero) doit être retournée.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

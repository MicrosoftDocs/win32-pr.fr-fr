---
description: 'En savoir plus sur : méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)'
title: Méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100731
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25e8430931cbf45c84d65fb68ae877ed96e7cea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862226"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string-int32"></a>Méthode API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)

Obtient les options de configuration de base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As IntPtr, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref IntPtr paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance de à partir de laquelle récupérer les options.

<!-- end list -->

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - paramid  
    Type : [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Paramètre à récupérer.

<!-- end list -->

  - Valeur paramValue  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Retourne la valeur du paramètre, si la valeur est un entier.

<!-- end list -->

  - paramString  
    Type : [System. String](/dotnet/api/system.string)  
    
    Retourne la valeur du paramètre, si la valeur est une chaîne.

<!-- end list -->

  - maxParam  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille maximale de la chaîne de paramètre.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Code d’avertissement ESENT.  

## <a name="remarks"></a>Notes

[ErrorToString](./jet-param-enumeration.md) passe le numéro d’erreur dans valeur paramValue, ce qui explique pourquoi il s’agit d’un paramètre ref et non d’un paramètre out.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetGetSystemParameter](./api.jetgetsystemparameter-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

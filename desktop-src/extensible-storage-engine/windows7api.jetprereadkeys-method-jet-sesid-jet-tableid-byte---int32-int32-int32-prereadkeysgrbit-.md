---
description: 'En savoir plus sur : méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, PrereadKeysGrbit)'
title: Méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. esent. Interop. d’un)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66f85c08c1fccc58702d4ac4cf170d6b0493ab8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033845"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a>Méthode Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, PrereadKeysGrbit)

Si les enregistrements avec les clés spécifiées ne se trouvent pas dans le cache des tampons, démarrez les lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.

**Espace de noms :**[Microsoft. ISAM. esent. Interop.](./microsoft.isam.esent.interop.windows7-namespace.md) une    
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Table avec laquelle émettre les prélectures.

<!-- end list -->

  - clés  
    Entrer \[\]  
    
    Clés à prélire. Les clés doivent être triées.

<!-- end list -->

  - Caractères de longueur  
    Entrer \[\]  
    
    Longueurs des clés à prélire.

<!-- end list -->

  - Nombre de frappes  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre maximal de clés à prélire.

<!-- end list -->

  - keysPreread  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne le nombre de clés à prélire réellement.

<!-- end list -->

  - grbit  
    Tapez : [Microsoft. ISAM. esent. Interop. PrereadKeysGrbit.](./prereadkeysgrbit-enumeration.md)  
    
    Options de prélecture. Utilisé pour spécifier la direction de la prélecture.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Windows7Api, classe](./windows7api-class.md)

[Membres Windows7Api](./windows7api-members.md)

[Surcharge JetPrereadKeys](./windows7api.jetprereadkeys-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop. les](./microsoft.isam.esent.interop.windows7-namespace.md)

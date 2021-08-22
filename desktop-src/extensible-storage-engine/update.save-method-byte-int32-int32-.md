---
description: 'En savoir plus sur : méthode Update. Save (Byte, Int32, Int32)'
title: Update. Save, méthode (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e586177075a34f3832486a9ace4a919abaad65dad21c0e54eba47b79f207be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603539"
---
# <a name="updatesave-method-byte--int32-int32"></a>Update. Save, méthode (Byte, Int32, Int32)

Mettez à jour TableID.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Paramètres

  - signet  
    Entrer \[\]  
    
    Retourne le signet de l’enregistrement mis à jour. Peut être Null.

<!-- end list -->

  - bookmarkSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la mémoire tampon du signet.

<!-- end list -->

  - actualBookmarkSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne la taille réelle du signet.

## <a name="remarks"></a>Remarques

L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, Update est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe de mise à jour](./update-class.md)

[Mettre à jour les membres](./update-members.md)

[Enregistrer la surcharge](./update.save-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

---
description: 'En savoir plus sur : méthode Update. SaveAndGotoBookmark'
title: Update. SaveAndGotoBookmark, méthode
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 566be9b1af403a794b6ac87259a0fd6b6c0fea46c0b45287c536f336ee734b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106953"
---
# <a name="updatesaveandgotobookmark-method"></a>Update. SaveAndGotoBookmark, méthode

Mettez à jour l’TableID et positionnez l’TableID sur l’enregistrement qui a été modifié. Cela peut être utile lors de l’insertion d’un enregistrement, car par défaut, TableID reste à son ancien emplacement.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>Notes

L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, Update est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe de mise à jour](./update-class.md)

[Mettre à jour les membres](./update-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

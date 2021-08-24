---
description: 'En savoir plus sur : Update. Save, méthode'
title: Update. Save, méthode
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890060"
---
# <a name="updatesave-method"></a>Update. Save, méthode

Mettez à jour TableID.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>Notes

L’enregistrement est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler la création d’un objet de mise à jour, puis en appelant JetSetColumn ou JetSetColumns une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, Update est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par Update ou et non pendant JetSetColumn ou JetSetColumns.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe de mise à jour](./update-class.md)

[Mettre à jour les membres](./update-members.md)

[Enregistrer la surcharge](./update.save-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

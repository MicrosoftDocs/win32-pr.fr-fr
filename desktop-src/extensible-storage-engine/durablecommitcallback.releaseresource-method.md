---
description: 'En savoir plus sur : méthode DurableCommitCallback. ReleaseResource'
title: Méthode DurableCommitCallback. ReleaseResource (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 758c27b1b3a67b91b7921276ec26e9c9776b65255c4cfa88d32b839f9950c2af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725269"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>Méthode DurableCommitCallback. ReleaseResource

Libère la session de validation durable.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a>Notes

N’essayez pas de définir le paramètre d’instance sur null, car le rappel est supprimé après JetTerm et le rappel ne peut pas être défini après JetTerm.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[DurableCommitCallback, classe](./durablecommitcallback-class.md)

[Membres DurableCommitCallback](./durablecommitcallback-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)

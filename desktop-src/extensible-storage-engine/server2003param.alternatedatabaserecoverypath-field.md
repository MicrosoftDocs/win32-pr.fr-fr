---
description: 'En savoir plus sur : champ Server2003Param. AlternateDatabaseRecoveryPath'
title: Champ Server2003Param. AlternateDatabaseRecoveryPath (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a85673979a3b65d8c78ca06fae4496c11f8d2b31c810d411142e6c40bfd62cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107242"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Champ Server2003Param. AlternateDatabaseRecoveryPath

Le chemin d’accès complet à chaque base de données est conservé dans les journaux des transactions au moment de l’exécution. En règle générale, ces bases de données doivent rester à l’emplacement d’origine pour que la relecture des transactions fonctionne correctement. Ce paramètre peut être utilisé pour forcer la récupération après incident ou une opération de restauration pour rechercher les bases de données référencées dans le journal des transactions dans le dossier spécifié.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Server2003Param, classe](./server2003param-class.md)

[Membres Server2003Param](./server2003param-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

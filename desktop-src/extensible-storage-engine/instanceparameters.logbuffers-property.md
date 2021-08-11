---
description: 'En savoir plus sur : InstanceParameters. LogBuffers, propriété'
title: InstanceParameters. LogBuffers, propriété
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60fbf06d13a8252051830c9a91dd348c2a7295a63212b587bfac9905b3b5903a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255960"
---
# <a name="instanceparameterslogbuffers-property"></a>InstanceParameters. LogBuffers, propriété

Obtient ou définit la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions. L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions. La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité. Ce paramètre a un impact sur les performances. Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide. Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée. La valeur par défaut est trop petite pour ce cas. Ne définissez pas ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

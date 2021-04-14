---
title: Implémentation de File-Based ILockBytes
description: Implémenté sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçu pour lire et écrire directement dans un fichier sur disque.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implémentations, basé sur des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379689"
---
# <a name="ilockbytes---file-based-implementation"></a>Implémentation de File-Based ILockBytes

Implémenté sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçu pour lire et écrire directement dans un fichier sur disque.

## <a name="when-to-use"></a>Quand l’utiliser

Les méthodes de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont appelées à partir des implémentations de fichiers composés de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sur l’objet de stockage de fichiers composés créé via un appel à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile). vous n’avez donc pas besoin de les appeler directement.

## <a name="remarks"></a>Notes

Voici les méthodes de l’implémentation de File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes :: readatum**
</dt> <dd>

Lit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes :: WriteAt**
</dt> <dd>

Écrit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes :: Flush**
</dt> <dd>

Garantit que toutes les mémoires tampons internes gérées par l’implémentation [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont écrites dans le stockage physique sous-jacent.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes :: configure**
</dt> <dd>

Définit la taille du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes :: LockRegion**
</dt> <dd>

Le paramètre *dwLockTypes* est défini sur lock \_ ONLYONCE ou Lock \_ exclusive, ce qui autorise ou limite l’accès aux régions verrouillées.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes :: UnlockRegion**
</dt> <dd>

Cette méthode déverrouille la région verrouillée par [**ILockBytes :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes :: stat**
</dt> <dd>

L’implémentation [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fournie par com appelle la méthode [**ILockBytes :: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) pour récupérer les informations sur l’objet de tableau d’octets. S’il n’existe pas de nom raisonnable pour le tableau d’octets, la méthode **ILockBytes :: stat** fournie par com retourne **null** dans le membre **pwcsName** de la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 





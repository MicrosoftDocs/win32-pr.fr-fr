---
title: ILockBytes-implémentation de la mémoire globale
description: L’implémentation de la mémoire globale ILockBytes est implémentée sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçue pour lire et écrire directement dans la mémoire globale.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implémentations, mémoire globale
- ILockBytes Strctd STG, implémentations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f9786f29433bcc02e0b56f3ea9d45c949593f60962e80a650d80ed625da41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867447"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes-implémentation de la mémoire globale

L’implémentation de la mémoire globale ILockBytes est implémentée sur un objet de tableau d’octets sous-jacent à un objet de stockage de fichiers composés COM et conçue pour lire et écrire directement dans la mémoire globale.

## <a name="when-to-use"></a>Quand l’utiliser

Les méthodes de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sont appelées à partir des implémentations de fichiers composés de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sur l’objet de stockage de fichiers composés créé via un appel à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).

## <a name="remarks"></a>Remarques

Voici les méthodes de l’implémentation de la mémoire globale [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes :: readatum**
</dt> <dd>

Lit un bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes :: WriteAt**
</dt> <dd>

Écrit le bloc d’octets à partir d’un offset spécifié au début du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes :: Flush**
</dt> <dd>

Contrairement à l’implémentation basée sur les fichiers, l’appel de cette méthode dans l’implémentation de la mémoire globale n’a aucun effet.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes :: configure**
</dt> <dd>

Définit la taille du tableau d’octets.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes :: LockRegion**
</dt> <dd>

Cette implémentation ne prend pas en charge le verrouillage, donc *dwLocksType* a la valeur zéro. L’appelant doit s’assurer que les accès sont valides et s’excluent mutuellement.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes :: UnlockRegion**
</dt> <dd>

Cette implémentation ne prend pas en charge le verrouillage.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes :: stat**
</dt> <dd>

L’implémentation [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fournie par com appelle la méthode [**ILockBytes :: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) pour récupérer des données sur l’objet de tableau d’octets. S’il n’existe pas de nom raisonnable pour le tableau d’octets, la méthode **ILockBytes :: stat** fournie par com retourne **null** dans le membre **pwcsName** de la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 





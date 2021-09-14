---
description: La classe CMediaType gère les types de média. Cette classe hérite de la \_ structure du type de média am \_ . Il peut être casté en une variable de type de \_ média am \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: CMediaType, classe (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195631"
---
# <a name="cmediatype-class"></a>CMediaType, classe

![hiérarchie de la classe cmediatype](images/mtype01.png)

La `CMediaType` classe gère les types de média. Cette classe hérite de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il peut être casté en une variable de type de **\_ média \_ am**.



| M&#233;thodes publiques                                                      | Description                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Méthode de constructeur.                                                            |
| [**~ CMediaType**](cmediatype--cmediatype.md)                       | Méthode de destructeur.                                                             |
| [**Définie**](cmediatype-set.md)                                       | Définit le type de média à partir d’un autre type de média.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Détermine si un type principal a été assigné à cet objet.              |
| [**Entrer**](cmediatype-type.md)                                     | Récupère le type principal.                                                      |
| [**SetType**](cmediatype-settype.md)                               | Spécifie le type principal.                                                      |
| [**Subtype**](cmediatype-subtype.md)                               | Récupère le sous-type.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Spécifie le sous-type.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Détermine si les échantillons ont une taille fixe ou une taille variable.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Détermine si le flux utilise la compression temporelle.                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | Récupère la taille de l’échantillon.                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | Spécifie une taille d’échantillon fixe ou spécifie que les échantillons ont une taille variable. |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | Spécifie que les exemples n’ont pas de taille fixe.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Spécifie si les échantillons sont compressés à l’aide de la compression temporelle.           |
| [**Format**](cmediatype-format.md)                                 | Récupère un pointeur vers le bloc de format.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Récupère la longueur du bloc de format.                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | Spécifie le type de format.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Récupère le type de format.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Spécifie le bloc de format.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Supprime le bloc de format.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Alloue de la mémoire pour le bloc de format.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Réaffecte le bloc de format à une nouvelle taille.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Initialise le type de média.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Détermine si ce type de média correspond à un type de média partiellement spécifié.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Détermine si le type de média est partiellement défini.                             |
| Opérateurs                                                           | Description                                                                    |
| [**opérateur =**](cmediatype-operator-.md)                          | Surcharge l’opérateur d’assignation pour copier un type de média.                        |
| [**opérateur = =**](cmediatype-operator--.md)                        | Vérifie l’égalité d’objets `CMediaType`.                               |
| [**opérateur ! =**](cmediatype-operator-neq.md)                      | Vérifie l’inégalité d’objets `CMediaType`.                             |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 





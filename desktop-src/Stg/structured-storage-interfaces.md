---
title: Interfaces de Stockage structurées
description: les services de Stockage structurés sont organisés en trois catégories d’interfaces.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfaces de Stockage structurées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345c7b10ae4f73a80b3a263b9a9487c2172382b176404871b363aff336441a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661719"
---
# <a name="structured-storage-interfaces"></a>Interfaces de Stockage structurées

les services de Stockage structurés sont organisés en trois catégories d' [interfaces](interfaces.md). Chaque ensemble représente un niveau d’indirection ou d’abstraction successif entre un fichier composé, les objets qu’il contient et le support physique dans lequel ces composants individuels sont stockés.

La première catégorie d’interfaces se compose de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)et [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). Les deux premières interfaces définissent la façon dont les objets sont stockés dans un fichier composé. Ces interfaces fournissent des méthodes permettant d’ouvrir des éléments de stockage, de valider et de rétablir des modifications, de copier et de déplacer des éléments, ainsi que de lire et d’écrire des flux. Ces interfaces ne reconnaissent pas les formats de données natifs des objets individuels et, par conséquent, n’ont aucune méthode pour enregistrer ces objets dans un stockage persistant. L’interface **IRootStorage** dispose d’une méthode unique pour associer un document composé à un nom de système de fichiers sous-jacent. Les clients doivent implémenter ces interfaces pour leurs fichiers composés.

La deuxième catégorie d’interfaces se compose des interfaces [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) , que les objets implémentent pour gérer leurs données persistantes. Ces interfaces fournissent des méthodes pour lire les formats de données d’objets individuels et savent donc comment les stocker. Les objets sont responsables de l’implémentation de ces interfaces, car les clients ne connaissent pas les formats de données natifs de leurs objets imbriqués. Ces interfaces n’ont toutefois aucune connaissance d’un support de stockage physique spécifique.

Une troisième catégorie se compose d’une seule interface, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), qui fournit des méthodes pour écrire des fichiers sur un support physique spécifique, tel qu’un disque dur ou un lecteur de bande. Toutefois, la plupart des applications n’implémentent pas l’interface **ILockBytes** , car com fournit déjà des implémentations pour les deux situations les plus courantes, qui sont l’implémentation basée sur des fichiers et l’implémentation basée sur la mémoire. L’objet de stockage de fichiers composés appelle les méthodes **ILockBytes** que vous ne les appelez pas directement dans l’implémentation.

## <a name="compound-file-implementation-limits"></a>Limites d’implémentation des fichiers composés

l’implémentation COM de l’architecture Stockage structurée est appelée *fichiers composés*. Stockage objets, tels qu’ils sont implémentés dans des fichiers composés, incluent une implémentation des interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

Les pointeurs vers l’implémentation de fichier composé de ces interfaces sont acquis en appelant la fonction [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) pour créer un objet de fichier composé, ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) pour ouvrir un fichier composé créé précédemment.

Une autre méthode pour acquérir un pointeur vers l’implémentation de fichier composé de ces interfaces consiste à appeler la fonction [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) plus ancienne et plus limitée. Les quatre fonctions sont traitées comme des implémentations de fichiers composés.

L’implémentation de fichier composé peut être configurée pour utiliser des secteurs d’octets 512 ou 4096, comme défini dans la structure [**STGOPTIONS**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) .

L’implémentation de fichier composé de fichiers composés est soumise aux contraintes d’implémentation suivantes.



| Limite                                           | Fichier composé                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limites de taille de fichier :                               | 512:2 gigaoctets (Go) 4096 : limites maximales du système de fichiers<br/>                                                                                                                    |
| Taille maximale du tas requise pour les éléments ouverts :   | 512:4 mégaoctets (Mo) 4096 : limites de la mémoire virtuelle maximale<br/>                                                                                                                 |
| La racine simultanée s’ouvre (ouvre le même fichier) : | Si \_ les STGM lecture et STGM \_ partage \_ refuser \_ l’écriture sont spécifiées, les limites sont dictées par les limites du système de fichiers. Dans le cas contraire, il y a une limite de 20 ouvertures de racine simultanées du même fichier. |
| Nombre d’éléments dans un fichier :                   | 512 : illimité, mais les performances peuvent se dégrader si le nombre d’éléments dans les milliers 4096 : illimité<br/>                                                                         |



 

En raison de la limite de taille de tas de 4 Mo, le nombre d’éléments ouverts en mode traité est généralement limité à plusieurs milliers d’éléments.

 


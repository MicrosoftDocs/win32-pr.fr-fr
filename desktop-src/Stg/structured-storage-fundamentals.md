---
title: Notions de base sur le stockage structuré
description: Le stockage structuré fournit l’équivalent d’un système de fichiers complet pour le stockage des objets.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Stockage structuré Strctd STG, notions de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842417"
---
# <a name="structured-storage-fundamentals"></a>Notions de base sur le stockage structuré

Le stockage structuré fournit l’équivalent d’un système de fichiers complet pour le stockage des objets via les éléments énumérés dans le tableau suivant.



| Élément                                                                  | Description                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de stockage structuré](structured-storage-interfaces.md)       | Les interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)et [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , ainsi qu’un ensemble d’interfaces associées ([**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)et [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)). |
| [Fonctions de l’API de stockage structuré](structured-storage-api-functions.md) | API d’assistance qui facilitent l’implémentation du stockage structuré, ainsi qu’un deuxième ensemble d’API pour les fichiers composés ; Il s’agit de l’implémentation COM des interfaces de stockage structuré. COM fournit également un ensemble de structures de prise en charge et de valeurs d’énumération utilisées pour organiser des paramètres pour les méthodes d’interface et les API.                              |
| [Modes d’accès de stockage structuré](structured-storage-access-modes.md)   | Ensemble de modes d’accès pour la régulation de l’accès aux fichiers composés.                                                                                                                                                                                                                                                                                                 |



 

 

 
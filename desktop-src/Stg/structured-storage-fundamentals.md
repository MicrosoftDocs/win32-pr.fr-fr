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
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="7a551-104">Notions de base sur le stockage structuré</span><span class="sxs-lookup"><span data-stu-id="7a551-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="7a551-105">Le stockage structuré fournit l’équivalent d’un système de fichiers complet pour le stockage des objets via les éléments énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7a551-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="7a551-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7a551-106">Element</span></span>                                                                  | <span data-ttu-id="7a551-107">Description</span><span class="sxs-lookup"><span data-stu-id="7a551-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a551-108">Interfaces de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="7a551-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="7a551-109">Les interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)et [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , ainsi qu’un ensemble d’interfaces associées ([**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)et [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)).</span><span class="sxs-lookup"><span data-stu-id="7a551-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="7a551-110">Fonctions de l’API de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="7a551-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="7a551-111">API d’assistance qui facilitent l’implémentation du stockage structuré, ainsi qu’un deuxième ensemble d’API pour les fichiers composés ; Il s’agit de l’implémentation COM des interfaces de stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="7a551-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="7a551-112">COM fournit également un ensemble de structures de prise en charge et de valeurs d’énumération utilisées pour organiser des paramètres pour les méthodes d’interface et les API.</span><span class="sxs-lookup"><span data-stu-id="7a551-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="7a551-113">Modes d’accès de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="7a551-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="7a551-114">Ensemble de modes d’accès pour la régulation de l’accès aux fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="7a551-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 
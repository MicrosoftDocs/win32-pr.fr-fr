---
title: Conventions d’affectation de noms aux objets de stockage
description: Les objets de stockage et de flux sont nommés selon un ensemble de conventions.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Stockage structuré Strctd STG, notions de base, conventions d’affectation des noms d’objets de stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379681"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="c35b7-104">Conventions d’affectation de noms aux objets de stockage</span><span class="sxs-lookup"><span data-stu-id="c35b7-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="c35b7-105">Les objets de stockage et de flux sont nommés selon un ensemble de conventions.</span><span class="sxs-lookup"><span data-stu-id="c35b7-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="c35b7-106">Le nom d’un objet de stockage racine est le nom réel du fichier dans le système de fichiers sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="c35b7-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="c35b7-107">Il est conforme aux conventions et aux restrictions imposées par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c35b7-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="c35b7-108">Les chaînes de nom de fichier passées aux méthodes et aux méthodes liées au stockage sont passées sur le système de fichiers, non interprétées et inchangées.</span><span class="sxs-lookup"><span data-stu-id="c35b7-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="c35b7-109">Le nom d’un élément imbriqué contenu dans un objet de stockage est géré par l’implémentation de l’objet de stockage particulier.</span><span class="sxs-lookup"><span data-stu-id="c35b7-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="c35b7-110">Toutes les implémentations des objets de stockage doivent prendre en charge les noms d’éléments imbriqués 32 caractères de longueur (y compris la marque de fin **null** ), bien que certaines implémentations puissent prendre en charge des noms plus longs.</span><span class="sxs-lookup"><span data-stu-id="c35b7-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="c35b7-111">Si l’objet de stockage effectue une conversion de casse quelconque est défini par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="c35b7-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="c35b7-112">Par conséquent, les applications qui définissent des noms d’élément doivent choisir des noms acceptables, que la conversion de casse soit effectuée ou non.</span><span class="sxs-lookup"><span data-stu-id="c35b7-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="c35b7-113">L’implémentation COM des fichiers composés prend en charge les noms d’une longueur maximale de 32 caractères et n’effectue aucune conversion de casse.</span><span class="sxs-lookup"><span data-stu-id="c35b7-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 





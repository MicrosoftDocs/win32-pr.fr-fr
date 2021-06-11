---
description: Découvrez comment créer un gestionnaire de propriétés qui lit et écrit des propriétés vers et à partir d’un flux de fichier. Chaque gestionnaire est associé à un type de fichier donné.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implémentation de gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989264"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="d38fa-104">Implémentation de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="d38fa-104">Implementing Property Handlers</span></span>

<span data-ttu-id="d38fa-105">Dans Windows Vista et versions ultérieures, les métadonnées sont devenues centrales comme une méthode d’organisation d’éléments tels que des fichiers, des messages électroniques ou des contacts.</span><span class="sxs-lookup"><span data-stu-id="d38fa-105">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="d38fa-106">Pour activer un système où les éléments peuvent être recherchés en fonction de leurs métadonnées et où les utilisateurs peuvent lire ou écrire ces métadonnées, Windows Vista a introduit un nouveau système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d38fa-106">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="d38fa-107">Les métadonnées de ce système sont représentées par un ensemble extensible de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d38fa-107">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="d38fa-108">Dans cet ensemble de rubriques, nous décrivons comment vous pouvez créer un gestionnaire qui lit et écrit des propriétés vers et à partir d’un flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="d38fa-108">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="d38fa-109">Ces gestionnaires sont appelés gestionnaires de propriétés et chacun d’eux est associé à un type de fichier donné, identifié par l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="d38fa-109">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="d38fa-110">Les rubriques suivantes décrivent les exigences et les stratégies impliquées dans la définition de vos propriétés et gestionnaires de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d38fa-110">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="d38fa-111">Fonctionnement des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="d38fa-111">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="d38fa-112">Utilisation des noms de genres</span><span class="sxs-lookup"><span data-stu-id="d38fa-112">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="d38fa-113">Utilisation des listes de propriétés</span><span class="sxs-lookup"><span data-stu-id="d38fa-113">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="d38fa-114">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="d38fa-114">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="d38fa-115">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="d38fa-115">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="d38fa-116">Meilleures pratiques pour le gestionnaire de propriétés et FAQ</span><span class="sxs-lookup"><span data-stu-id="d38fa-116">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="d38fa-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d38fa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d38fa-118">Création de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="d38fa-118">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="d38fa-119">Schéma de la description de propriété</span><span class="sxs-lookup"><span data-stu-id="d38fa-119">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 

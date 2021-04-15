---
description: Dans Windows Vista et versions ultérieures, les métadonnées sont devenues centrales comme une méthode d’organisation d’éléments tels que des fichiers, des messages électroniques ou des contacts.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implémentation de gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203855"
---
# <a name="implementing-property-handlers"></a><span data-ttu-id="b58b2-103">Implémentation de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="b58b2-103">Implementing Property Handlers</span></span>

<span data-ttu-id="b58b2-104">Dans Windows Vista et versions ultérieures, les métadonnées sont devenues centrales comme une méthode d’organisation d’éléments tels que des fichiers, des messages électroniques ou des contacts.</span><span class="sxs-lookup"><span data-stu-id="b58b2-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="b58b2-105">Pour activer un système où les éléments peuvent être recherchés en fonction de leurs métadonnées et où les utilisateurs peuvent lire ou écrire ces métadonnées, Windows Vista a introduit un nouveau système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b58b2-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="b58b2-106">Les métadonnées de ce système sont représentées par un ensemble extensible de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b58b2-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="b58b2-107">Dans cet ensemble de rubriques, nous décrivons comment vous pouvez créer un gestionnaire qui lit et écrit des propriétés vers et à partir d’un flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="b58b2-107">In this set of topics we describe how you can create a handler that reads and writes properties to and from a file stream.</span></span> <span data-ttu-id="b58b2-108">Ces gestionnaires sont appelés gestionnaires de propriétés et chacun d’eux est associé à un type de fichier donné, identifié par l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="b58b2-108">These handlers are called property handlers and each is associated with a given file types, identified by the file name extension.</span></span>

<span data-ttu-id="b58b2-109">Les rubriques suivantes décrivent les exigences et les stratégies impliquées dans la définition de vos propriétés et gestionnaires de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b58b2-109">The following topics discuss the requirements and strategies involved in defining your properties and property handlers.</span></span>

-   [<span data-ttu-id="b58b2-110">Fonctionnement des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="b58b2-110">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
-   [<span data-ttu-id="b58b2-111">Utilisation des noms de genres</span><span class="sxs-lookup"><span data-stu-id="b58b2-111">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
-   [<span data-ttu-id="b58b2-112">Utilisation des listes de propriétés</span><span class="sxs-lookup"><span data-stu-id="b58b2-112">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
-   [<span data-ttu-id="b58b2-113">Initialisation des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="b58b2-113">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
-   [<span data-ttu-id="b58b2-114">Inscription et distribution des gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="b58b2-114">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
-   [<span data-ttu-id="b58b2-115">Meilleures pratiques pour le gestionnaire de propriétés et FAQ</span><span class="sxs-lookup"><span data-stu-id="b58b2-115">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)

## <a name="related-topics"></a><span data-ttu-id="b58b2-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b58b2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b58b2-117">Création de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="b58b2-117">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="b58b2-118">Schéma de la description de propriété</span><span class="sxs-lookup"><span data-stu-id="b58b2-118">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 

---
description: Découvrez les scénarios de développement pour les propriétés personnalisées et les gestionnaires de propriétés dans le système de propriétés Windows.
ms.assetid: 3281736b-f9ea-4699-a128-3bce6810126e
title: Guide du développeur de système de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a26044d0d457d4ba24b8c9a18555885c12a571
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988924"
---
# <a name="property-system-developers-guide"></a><span data-ttu-id="8046f-103">Guide du développeur de système de propriétés</span><span class="sxs-lookup"><span data-stu-id="8046f-103">Property System Developer's Guide</span></span>

<span data-ttu-id="8046f-104">Dans Windows Vista et versions ultérieures, les métadonnées sont devenues centrales comme une méthode d’organisation d’éléments tels que des fichiers, des messages électroniques ou des contacts.</span><span class="sxs-lookup"><span data-stu-id="8046f-104">In Windows Vista and later, metadata became central as a method of organizing items such as files, e-mail, or contacts.</span></span> <span data-ttu-id="8046f-105">Pour activer un système où les éléments peuvent être recherchés en fonction de leurs métadonnées et où les utilisateurs peuvent lire ou écrire ces métadonnées, Windows Vista a introduit un nouveau système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8046f-105">To enable a system where items can be searched based on their metadata and where users can read or write that metadata, Windows Vista introduced a new property system.</span></span> <span data-ttu-id="8046f-106">Les métadonnées de ce système sont représentées par un ensemble extensible de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8046f-106">Metadata in this system is represented by an extensible set of properties.</span></span> <span data-ttu-id="8046f-107">Avec l’introduction des propriétés dans Windows Vista qui ont fait abstraction les spécificités des éléments tels que les photos, la musique, les documents, les messages, les contacts et les fichiers, les éditeurs de logiciels indépendants (ISV) peuvent désormais présenter leurs propres propriétés à la plateforme si aucune propriété existante ne répond à leurs besoins.</span><span class="sxs-lookup"><span data-stu-id="8046f-107">With the introduction of properties in Windows Vista that abstracted the specifics of items such as photos, music, documents, messages, contacts, and files, Independent software vendors (ISVs) can now introduce their own properties to the platform if no existing property meets their needs.</span></span>

<span data-ttu-id="8046f-108">Cette section décrit les scénarios de développement suivants dans le système de propriétés Windows :</span><span class="sxs-lookup"><span data-stu-id="8046f-108">This section describes the following development scenarios within the Windows Property System:</span></span>

-   [<span data-ttu-id="8046f-109">Création de propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="8046f-109">Creating Custom Properties</span></span>](./building-property-handlers-property-schemas.md)
-   [<span data-ttu-id="8046f-110">Implémentation de gestionnaires de propriétés</span><span class="sxs-lookup"><span data-stu-id="8046f-110">Implementing Property Handlers</span></span>](./building-property-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="8046f-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8046f-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8046f-112">Cliquez sur [Vue d’ensemble du système de propriétés](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8046f-112">[Property System Overview](property-system-overview.md)</span></span>
</dt> <dt>

[<span data-ttu-id="8046f-113">Référence du système de propriétés</span><span class="sxs-lookup"><span data-stu-id="8046f-113">Property System Reference</span></span>](property-system-reference.md)
</dt> <dt>

[<span data-ttu-id="8046f-114">Exemples de code du système de propriétés</span><span class="sxs-lookup"><span data-stu-id="8046f-114">Property System Code Samples</span></span>](property-system-code-samples.md)
</dt> </dl>

 

 

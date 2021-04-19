---
description: Les catégories vous aident à organiser les événements afin que les observateur d’événements puissent les filtrer. Chaque source d’événement peut définir ses propres catégories numérotées et les chaînes de texte auxquelles elles sont mappées.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Catégories d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516935"
---
# <a name="event-categories"></a><span data-ttu-id="3318d-104">Catégories d’événements</span><span class="sxs-lookup"><span data-stu-id="3318d-104">Event Categories</span></span>

<span data-ttu-id="3318d-105">Les catégories vous aident à organiser les événements afin que les observateur d’événements puissent les filtrer.</span><span class="sxs-lookup"><span data-stu-id="3318d-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="3318d-106">Chaque [source d’événement](event-sources.md) peut définir ses propres catégories numérotées et les chaînes de texte auxquelles elles sont mappées.</span><span class="sxs-lookup"><span data-stu-id="3318d-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="3318d-107">Les catégories doivent être numérotées consécutivement, en commençant par le chiffre 1.</span><span class="sxs-lookup"><span data-stu-id="3318d-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="3318d-108">Les catégories elles-mêmes sont définies dans un fichier de message.</span><span class="sxs-lookup"><span data-stu-id="3318d-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="3318d-109">Par exemple, utilisez la syntaxe suivante pour déclarer trois catégories d’événements.</span><span class="sxs-lookup"><span data-stu-id="3318d-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="3318d-110">Dans observateur d’événements, les événements qui utilisent ces catégories auront la catégorie 1, la catégorie 2 ou la catégorie 3 affichée dans la colonne **catégorie** .</span><span class="sxs-lookup"><span data-stu-id="3318d-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="3318d-111">Les catégories peuvent être stockées dans un fichier de message distinct ou dans un fichier qui contient des messages d’autres types.</span><span class="sxs-lookup"><span data-stu-id="3318d-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="3318d-112">Si vous créez un seul fichier de message, assurez-vous que les catégories sont les premiers messages du fichier.</span><span class="sxs-lookup"><span data-stu-id="3318d-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="3318d-113">Pour plus d’informations sur la création et l’utilisation de fichiers de messages, consultez [fichiers de messages](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="3318d-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="3318d-114">Le nombre total de catégories est stocké dans la valeur **CategoryCount** pour la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="3318d-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 




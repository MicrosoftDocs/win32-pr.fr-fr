---
description: Chaque événement peut être associé à des données spécifiques à l’événement.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Données d'événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516934"
---
# <a name="event-data"></a><span data-ttu-id="1f406-103">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="1f406-103">Event Data</span></span>

<span data-ttu-id="1f406-104">Chaque événement peut être associé à des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1f406-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="1f406-105">Le observateur d’événements n’interprète pas ces données ; il affiche des données supplémentaires uniquement dans un format de texte et hexadécimal combiné.</span><span class="sxs-lookup"><span data-stu-id="1f406-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="1f406-106">La limite maximale de la taille d’un événement dans le journal pair est de 0x3FFFF octets.</span><span class="sxs-lookup"><span data-stu-id="1f406-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="1f406-107">Par conséquent, utilisez des données spécifiques aux événements avec modération, y compris uniquement si vous êtes certain qu’elles seront utiles pour le débogage d’un problème.</span><span class="sxs-lookup"><span data-stu-id="1f406-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="1f406-108">Par exemple, de nombreux événements liés au réseau incluent des blocs de contrôle réseau (NCB) en tant que données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1f406-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="1f406-109">Lorsque vous utilisez des données spécifiques à un événement, la dernière partie de sa chaîne de description doit fournir une note sur les informations fournies sous forme de données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1f406-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="1f406-110">Par exemple, le logiciel réseau peut fournir une note telle que : « (le NCB est les données d’événement.) » En guise de Convention, utilisez des parenthèses autour de ces remarques, comme indiqué dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="1f406-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="1f406-111">Vous pouvez également utiliser des données spécifiques aux événements pour stocker des informations que l’application peut traiter indépendamment de la observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="1f406-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="1f406-112">Par exemple, vous pouvez écrire une visionneuse spécifique pour vos événements ou écrire un programme qui analyse le journal et crée un rapport qui contient des informations à partir des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="1f406-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 




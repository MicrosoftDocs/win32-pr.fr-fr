---
description: La visionneuse de frames Moniteur réseau affiche les données analysées dans trois volets.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Affichage des informations analysées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567409"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="9473b-103">Affichage des informations analysées</span><span class="sxs-lookup"><span data-stu-id="9473b-103">Viewing Parsed Information</span></span>

<span data-ttu-id="9473b-104">La visionneuse de frames Moniteur réseau affiche les données analysées dans trois volets.</span><span class="sxs-lookup"><span data-stu-id="9473b-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="9473b-105">Le volet supérieur affiche un résumé du frame qui comprend le protocole identifié.</span><span class="sxs-lookup"><span data-stu-id="9473b-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="9473b-106">Le volet central affiche les propriétés de données mises en forme qui peuvent être organisées hiérarchiquement dans le cadre de l’affichage de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="9473b-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="9473b-107">Le volet inférieur affiche les données brutes en surbrillance sélectionnées dans le volet central.</span><span class="sxs-lookup"><span data-stu-id="9473b-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="9473b-108">Vous pouvez spécifier le mode d’affichage des informations dans la visionneuse lorsque vous développez votre propre analyseur.</span><span class="sxs-lookup"><span data-stu-id="9473b-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="9473b-109">L’illustration suivante montre comment les informations peuvent être affichées dans la visionneuse de frames Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9473b-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![visionneuse de trames du moniteur réseau](images/parseui.png)

> [!Note]  
> <span data-ttu-id="9473b-111">Les analyseurs n’affichent pas les frames.</span><span class="sxs-lookup"><span data-stu-id="9473b-111">Parsers do not display frames.</span></span> <span data-ttu-id="9473b-112">Les analyseurs reconnaissent les champs dans les informations fournies, puis notifient Moniteur réseau pour afficher le frame.</span><span class="sxs-lookup"><span data-stu-id="9473b-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="9473b-113">Le filtrage est une opération de niveau supérieur qui permet aux requêtes de filtre d’étendre des analyseurs.</span><span class="sxs-lookup"><span data-stu-id="9473b-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="9473b-114">Dans votre analyseur, utilisez uniquement les fonctions qui peuvent s’exécuter sur les applications Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="9473b-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="9473b-115">Avant d’attacher des propriétés aux données brutes, un analyseur doit d’abord inscrire toutes les propriétés possibles avec le noyau Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9473b-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="9473b-116">L’analyseur envoie un message au noyau pour créer une base de données de propriétés, puis remplit la base de données de propriétés avec chaque propriété possible pour son protocole.</span><span class="sxs-lookup"><span data-stu-id="9473b-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="9473b-117">Chaque propriété de la base de données de propriété contient des informations telles qu’une description textuelle, un type de données et un qualificateur utilisés pour mettre en forme les données brutes, ainsi qu’une routine de mise en forme utilisée pour afficher les données.</span><span class="sxs-lookup"><span data-stu-id="9473b-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 




---
description: Une page de référence d’événement (ERP) est un document HTML qui fournit des informations Moniteur réseau sur les événements détectés pendant l’analyse ou l’opération de surveillance.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: À propos des pages de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865469"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="20ce9-103">À propos des pages de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="20ce9-103">About Event Reference Pages</span></span>

<span data-ttu-id="20ce9-104">Une page de référence d’événement (ERP) est un document HTML qui fournit des informations Moniteur réseau sur les événements détectés pendant l’analyse ou l’opération de surveillance.</span><span class="sxs-lookup"><span data-stu-id="20ce9-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="20ce9-105">Vous pouvez afficher vos solutions ERP dans le observateur d’événements de Moniteur réseau, l’outil de contrôle de l’analyse ou un navigateur prenant en charge les fonctionnalités HTML de Microsoft Internet Explorer version 4,01 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="20ce9-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="20ce9-106">Autrement dit, vous pouvez ajouter des contrôles pris en charge ou des langages de script dans votre ERP.</span><span class="sxs-lookup"><span data-stu-id="20ce9-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="20ce9-107">Toutefois, vos solutions ERP s’affiche uniquement si l’expert désigne le document HTML par son nom.</span><span class="sxs-lookup"><span data-stu-id="20ce9-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="20ce9-108">Lorsqu’il est correctement désigné, l’ERP s’affiche dans le volet inférieur lorsque l’événement dans le observateur d’événements est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="20ce9-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="20ce9-109">La figure ci-dessous illustre une ERP associée à l’analyse de plage IP (Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="20ce9-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![une ERP associée à l’analyse de plage d’adresses IP](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="20ce9-111">Événements d’experts</span><span class="sxs-lookup"><span data-stu-id="20ce9-111">Expert Events</span></span>

<span data-ttu-id="20ce9-112">Les événements experts sont identifiés par le membre **EventIdent** d’une structure [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="20ce9-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="20ce9-113">Lorsque vous écrivez un expert, vous déterminez les valeurs de **EventIdent** , qui sont généralement numérotées 1, 2, 3, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="20ce9-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="20ce9-114">Supposons, par exemple, qu’un expert génère deux événements (**EventIdent1** et **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="20ce9-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="20ce9-115">Si vous souhaitez que les observateur d’événements affichent les événements séparément, vous devez créer deux documents ERP distincts.</span><span class="sxs-lookup"><span data-stu-id="20ce9-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 




---
description: Messages de qualité
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Messages de qualité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521327"
---
# <a name="quality-messages"></a><span data-ttu-id="11603-103">Messages de qualité</span><span class="sxs-lookup"><span data-stu-id="11603-103">Quality Messages</span></span>

<span data-ttu-id="11603-104">Les messages de qualité sont définis avec la structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="11603-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="11603-105">Cette structure contient les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="11603-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="11603-106">**Tapez :** Défini par l’énumération [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; soit famine, ce qui indique que le filtre reçoit trop peu de données, ou inondation, indiquant que le filtre reçoit trop de données.</span><span class="sxs-lookup"><span data-stu-id="11603-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="11603-107">**Proportion :** Ajustement demandé dans le débit de données, à partir d’une ligne de base de 1000.</span><span class="sxs-lookup"><span data-stu-id="11603-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="11603-108">Par exemple, 750 indique 75% et 1500 indique 150%.</span><span class="sxs-lookup"><span data-stu-id="11603-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="11603-109">**Tard :** Temps de référence indiquant la date à laquelle l’exemple le plus récent est arrivé.</span><span class="sxs-lookup"><span data-stu-id="11603-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="11603-110">La valeur est négative si l’exemple est arrivé tôt.</span><span class="sxs-lookup"><span data-stu-id="11603-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="11603-111">**Horodateur :** Horodatage de l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="11603-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="11603-112">Par exemple, supposons qu’un échantillon avec un horodatage de 240 millisecondes (MS) atteigne le convertisseur à 280 ms, temps de flux.</span><span class="sxs-lookup"><span data-stu-id="11603-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="11603-113">Le convertisseur crée un message de qualité de type famine.</span><span class="sxs-lookup"><span data-stu-id="11603-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="11603-114">L’exemple a atteint 40 ms en retard, donc le membre **tardif** est 400000.</span><span class="sxs-lookup"><span data-stu-id="11603-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="11603-115">(Toutes les durées de référence sont en unités de 100 nanosecondes.) Le membre **timestamp** est 2,4 millions.</span><span class="sxs-lookup"><span data-stu-id="11603-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="11603-116">Pour le membre de **proportion** , le convertisseur peut utiliser une moyenne en cours d’exécution pour calculer la valeur.</span><span class="sxs-lookup"><span data-stu-id="11603-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="11603-117">Des exemples ont peut-être été arrivés à l’heure et cet exemple est une anomalie.</span><span class="sxs-lookup"><span data-stu-id="11603-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="11603-118">Dans ce cas, le convertisseur peut demander uniquement une petite correction.</span><span class="sxs-lookup"><span data-stu-id="11603-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="11603-119">En revanche, si les échantillons sont constamment en retard, le convertisseur peut demander une plus grande correction.</span><span class="sxs-lookup"><span data-stu-id="11603-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="11603-120">Le contrôle de qualité est géré par le biais de l’interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="11603-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="11603-121">Il contient deux méthodes.</span><span class="sxs-lookup"><span data-stu-id="11603-121">It contains two methods.</span></span>

-   <span data-ttu-id="11603-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envoie un message de qualité.</span><span class="sxs-lookup"><span data-stu-id="11603-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="11603-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): spécifie un gestionnaire de qualité personnalisé.</span><span class="sxs-lookup"><span data-stu-id="11603-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="11603-124">Un objet qui implémente **IQualityControl** reçoit des messages de qualité par le biais de sa méthode **Notify** .</span><span class="sxs-lookup"><span data-stu-id="11603-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="11603-125">Il peut soit gérer le message, soit le transmettre à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="11603-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="11603-126">Si l’application appelle la méthode **SetSink** de l’objet, l’objet doit déléguer le contrôle de qualité au gestionnaire de qualité spécifié.</span><span class="sxs-lookup"><span data-stu-id="11603-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 




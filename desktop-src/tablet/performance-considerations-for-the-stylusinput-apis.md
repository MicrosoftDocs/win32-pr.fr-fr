---
description: Description des manières d’améliorer les performances lors de l’utilisation des interfaces de programmation d’applications (API) StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considérations relatives aux performances de l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759807"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="83f59-103">Considérations relatives aux performances de l’API StylusInput</span><span class="sxs-lookup"><span data-stu-id="83f59-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="83f59-104">La liste suivante décrit quelques méthodes permettant d’améliorer les performances des applications qui utilisent les API StylusInput.</span><span class="sxs-lookup"><span data-stu-id="83f59-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="83f59-105">Utilisez la propriété [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) pour vous abonner uniquement aux données pertinentes pour votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="83f59-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="83f59-106">Cela réduit le nombre total d’appels de méthode que l’objet [**RealTimeStylus**](realtimestylus-class.md) effectue et réduit également la complexité de votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="83f59-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="83f59-107">L’objet **RealTimeStylus** vérifie uniquement la propriété DataInterest lorsque le plug-in est attaché.</span><span class="sxs-lookup"><span data-stu-id="83f59-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="83f59-108">Réduisez la complexité des plug-ins synchrones. Les plug-ins synchrones sont généralement appelés par le thread de l’objet [**RealTimeStylus**](realtimestylus-class.md) et peuvent contribuer aux retards dans la collection d’encres.</span><span class="sxs-lookup"><span data-stu-id="83f59-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="83f59-109">Envisagez de rendre votre plug-in asynchrone.</span><span class="sxs-lookup"><span data-stu-id="83f59-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="83f59-110">Si votre plug-in est complexe et doit ajouter des données personnalisées à la file d’attente de l’objet [**RealTimeStylus**](realtimestylus-class.md) , envisagez d’utiliser un modèle **RealTimeStylus** monté en cascade et d’ajouter le plug-in à la collection de plug-in synchrone de l’objet **RealTimeStylus** secondaire.</span><span class="sxs-lookup"><span data-stu-id="83f59-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="83f59-111">Pour plus d’informations sur le modèle **RealTimeStylus** monté en cascade, consultez [le modèle RealTimeStylus monté en cascade](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="83f59-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 

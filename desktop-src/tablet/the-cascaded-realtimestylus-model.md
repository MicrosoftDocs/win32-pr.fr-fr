---
description: Vue d’ensemble du modèle en cascade pour la classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Modèle RealTimeStylus monté en cascade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557915"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="713ed-103">Modèle RealTimeStylus monté en cascade</span><span class="sxs-lookup"><span data-stu-id="713ed-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="713ed-104">Le modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade vous permet d’utiliser deux objets **RealTimeStylus** , chacun s’exécutant sur un thread différent.</span><span class="sxs-lookup"><span data-stu-id="713ed-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="713ed-105">Avec ce modèle, vous attachez un objet **RealTimeStylus** secondaire à un objet **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="713ed-106">L’objet **RealTimeStylus** secondaire est attaché en tant que seul plug-in asynchrone dans la collection de plug-in asynchrone de l’objet **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="713ed-107">Le modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade peut être utile dans les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="713ed-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="713ed-108">Vous pouvez ajouter certaines tâches qui peuvent être exigeantes en termes de calcul, tout en nécessitant un accès en temps réel au flux de données du stylet, tel que la reconnaissance de mouvement multitrait, à la collection de plug-ins synchrones de l’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire.</span><span class="sxs-lookup"><span data-stu-id="713ed-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="713ed-109">Vous pouvez répartir la charge de calcul de vos plug-ins synchrones sur deux threads, ce qui réduit les retards dans la collecte d’encre sur certains Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="713ed-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="713ed-110">Le diagramme suivant illustre le déroulement des données du stylet de tablette par le biais de deux objets [**RealTimeStylus**](realtimestylus-class.md) en cascade et de leurs collections de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="713ed-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![Illustration montrant le workflow de données RealTimeStylus en cascade](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="713ed-112">Dans ce diagramme, le cercle « A » représente les données du stylet de tablette qui ont déjà été traitées par les objets [**RealTimeStylus**](realtimestylus-class.md) principal et secondaire et qui a été placé dans la file d’attente de sortie de l’objet **RealTimeStylus** secondaire.</span><span class="sxs-lookup"><span data-stu-id="713ed-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="713ed-113">Le cercle « B » contient des données de stylet de tablette qui ont déjà été traitées par l’objet **RealTimeStylus** principal et ajoutées à la file d’attente de sortie de l’objet **RealTimeStylus** principal et qui n’ont pas encore été envoyées à l’objet **RealTimeStylus** secondaire.</span><span class="sxs-lookup"><span data-stu-id="713ed-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="713ed-114">Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="713ed-115">Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie.</span><span class="sxs-lookup"><span data-stu-id="713ed-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="713ed-116">Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="713ed-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="713ed-117">Contraintes</span><span class="sxs-lookup"><span data-stu-id="713ed-117">Constraints</span></span>

<span data-ttu-id="713ed-118">Si vous utilisez le constructeur [**RealTimeStylus**](realtimestylus-class.md) par défaut, vous créez un objet **RealTimeStylus** qui peut uniquement accepter l’entrée d’un autre objet **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="713ed-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="713ed-119">La liste suivante décrit les contraintes associées à l’utilisation du modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade.</span><span class="sxs-lookup"><span data-stu-id="713ed-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="713ed-120">Seuls deux objets [**RealTimeStylus**](realtimestylus-class.md) peuvent être utilisés, un objet **RealTimeStylus** principal et un objet **RealTimeStylus** secondaire.</span><span class="sxs-lookup"><span data-stu-id="713ed-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="713ed-121">L’objet [**RealTimeStylus**](realtimestylus-class.md) primaire doit être créé avec un constructeur qui utilise le paramètre **attachedControl** ou *handle* .</span><span class="sxs-lookup"><span data-stu-id="713ed-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="713ed-122">L’objet **RealTimeStylus** secondaire doit être créé avec le constructeur sans argument.</span><span class="sxs-lookup"><span data-stu-id="713ed-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="713ed-123">L’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire doit être le seul plug-in asynchrone dans la collection de plug-in asynchrone de l’objet **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="713ed-124">Un objet [**RealTimeStylus**](realtimestylus-class.md) secondaire ne peut être attaché qu’à un seul objet **RealTimeStylus** principal à la fois.</span><span class="sxs-lookup"><span data-stu-id="713ed-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="713ed-125">Si elle est ajoutée à un deuxième objet **RealTimeStylus** principal, la méthode [Add](/previous-versions/ms824814(v=msdn.10)) lève une exception et l’objet **RealTimeStylus** secondaire n’est pas attaché au deuxième objet **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="713ed-126">Le comportement de certains membres de l’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire est modifié.</span><span class="sxs-lookup"><span data-stu-id="713ed-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="713ed-127">Le tableau suivant décrit le comportement modifié de ces membres.</span><span class="sxs-lookup"><span data-stu-id="713ed-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="713ed-128">Membre</span><span class="sxs-lookup"><span data-stu-id="713ed-128">Member</span></span></th>
    <th><span data-ttu-id="713ed-129">Comportement</span><span class="sxs-lookup"><span data-stu-id="713ed-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="713ed-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="713ed-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="713ed-131">Cette méthode retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="713ed-132">Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, cette méthode retourne la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="713ed-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="713ed-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="713ed-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="713ed-134">Cette méthode lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="713ed-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="713ed-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="713ed-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="713ed-136">Cette méthode retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="713ed-137">Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, cette méthode retourne un tableau vide.</span><span class="sxs-lookup"><span data-stu-id="713ed-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="713ed-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="713ed-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="713ed-139">L’obtention de cette propriété retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="713ed-140">Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, l’obtention de cette propriété retourne la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="713ed-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="713ed-141">La définition de cette propriété lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="713ed-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="713ed-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span><span class="sxs-lookup"><span data-stu-id="713ed-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="713ed-143">L’obtention de cette propriété retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.</span><span class="sxs-lookup"><span data-stu-id="713ed-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="713ed-144">Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, l’obtention de cette propriété retourne la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="713ed-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="713ed-145">La définition de cette propriété lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="713ed-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="713ed-146">L’objet [**RealTimeStylus**](realtimestylus-class.md) parent est supposé cesser de fonctionner lorsque le **RealTimeStylus** enfant est supprimé.</span><span class="sxs-lookup"><span data-stu-id="713ed-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 

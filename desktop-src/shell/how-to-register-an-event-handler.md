---
description: Un appareil peut potentiellement générer un grand nombre d’événements, et chaque événement peut être géré par un certain nombre de gestionnaires différents.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Comment inscrire un gestionnaire d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973134"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="eef1d-103">Comment inscrire un gestionnaire d’événements</span><span class="sxs-lookup"><span data-stu-id="eef1d-103">How to Register an Event Handler</span></span>

<span data-ttu-id="eef1d-104">Un appareil peut potentiellement générer un grand nombre d’événements, et chaque événement peut être géré par un certain nombre de gestionnaires différents.</span><span class="sxs-lookup"><span data-stu-id="eef1d-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="eef1d-105">Dans Windows XP, les événements suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="eef1d-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="eef1d-106">DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-106">DeviceArrival</span></span>
-   <span data-ttu-id="eef1d-107">DeviceRemoval</span><span class="sxs-lookup"><span data-stu-id="eef1d-107">DeviceRemoval</span></span>
-   <span data-ttu-id="eef1d-108">MediaArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-108">MediaArrival</span></span>
-   <span data-ttu-id="eef1d-109">MediaRemoval</span><span class="sxs-lookup"><span data-stu-id="eef1d-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="eef1d-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="eef1d-110">Instructions</span></span>


<span data-ttu-id="eef1d-111">Les gestionnaires d’événements sont définis sous la clé **EventHandlers** .</span><span class="sxs-lookup"><span data-stu-id="eef1d-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="eef1d-112">Les valeurs d’une clé de gestionnaire d’événements sont les noms de chaque gestionnaire que l’utilisateur doit choisir lorsque l’événement est détecté.</span><span class="sxs-lookup"><span data-stu-id="eef1d-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="eef1d-113">Aucune valeur de données n’est associée à ces entrées.</span><span class="sxs-lookup"><span data-stu-id="eef1d-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="eef1d-114">Voici un exemple de définition d’un gestionnaire d’événements personnalisé appelé **MyNewRemovalEventHandler**, qui présente ces possibilités de gestionnaire à l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="eef1d-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="eef1d-115">Gestionnaire à utiliser si l’événement est détecté sur un appareil effectué par la société nommée Contoso, Inc.</span><span class="sxs-lookup"><span data-stu-id="eef1d-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="eef1d-116">Gestionnaire à utiliser si l’événement est détecté sur un appareil effectué par l’entreprise nommée Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="eef1d-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="eef1d-117">Gestionnaire à utiliser dans tous les autres cas.</span><span class="sxs-lookup"><span data-stu-id="eef1d-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="eef1d-118">Une fois qu’un gestionnaire d’événements est défini, il doit être inscrit auprès d’un gestionnaire d’appareils pour l’une des possibilités d’événement : DeviceArrival, DeviceRemoval, MediaArrival ou MediaRemoval.</span><span class="sxs-lookup"><span data-stu-id="eef1d-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="eef1d-119">MyNewRemovalEventHandler, défini précédemment, est utilisé pour DeviceRemoval sous un gestionnaire d’appareils personnalisé nommé MyDeviceHandler et est défini à cet effet dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="eef1d-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="eef1d-120">Là encore, la valeur de Registre n’a pas de composant de données.</span><span class="sxs-lookup"><span data-stu-id="eef1d-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="eef1d-121">Windows XP prédéfinit l’ensemble suivant d’EventHandlers.</span><span class="sxs-lookup"><span data-stu-id="eef1d-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="eef1d-122">Clé EventHandlers</span><span class="sxs-lookup"><span data-stu-id="eef1d-122">EventHandlers key</span></span>        | <span data-ttu-id="eef1d-123">Type de fichier ou de média</span><span class="sxs-lookup"><span data-stu-id="eef1d-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="eef1d-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="eef1d-125">CD-R/CD-RW vierge</span><span class="sxs-lookup"><span data-stu-id="eef1d-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="eef1d-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="eef1d-127">Fichiers image</span><span class="sxs-lookup"><span data-stu-id="eef1d-127">Picture files</span></span>                                  |
| <span data-ttu-id="eef1d-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="eef1d-129">Fichiers musicaux</span><span class="sxs-lookup"><span data-stu-id="eef1d-129">Music files</span></span>                                    |
| <span data-ttu-id="eef1d-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="eef1d-131">Fichiers vidéo</span><span class="sxs-lookup"><span data-stu-id="eef1d-131">Video files</span></span>                                    |
| <span data-ttu-id="eef1d-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="eef1d-133">CD audio (format de CD de format REDBOOK avec pistes audio)</span><span class="sxs-lookup"><span data-stu-id="eef1d-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="eef1d-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="eef1d-135">Films DVD</span><span class="sxs-lookup"><span data-stu-id="eef1d-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="eef1d-136">Windows Vista prédéfinit l’ensemble suivant d’EventHandlers, en plus de ceux ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="eef1d-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="eef1d-137">Clé EventHandlers</span><span class="sxs-lookup"><span data-stu-id="eef1d-137">EventHandlers key</span></span>              | <span data-ttu-id="eef1d-138">Type de fichier ou de média</span><span class="sxs-lookup"><span data-stu-id="eef1d-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="eef1d-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="eef1d-140">Films Super VideoCD</span><span class="sxs-lookup"><span data-stu-id="eef1d-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="eef1d-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="eef1d-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="eef1d-142">Films VideoCD</span><span class="sxs-lookup"><span data-stu-id="eef1d-142">VideoCD movies</span></span>       |



 

 

 




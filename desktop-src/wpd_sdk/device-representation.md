---
description: Représentation de l’appareil
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Représentation de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484737"
---
# <a name="device-representation"></a><span data-ttu-id="2a784-103">Représentation de l’appareil</span><span class="sxs-lookup"><span data-stu-id="2a784-103">Device Representation</span></span>

<span data-ttu-id="2a784-104">Les appareils ont deux comportements principaux qui sont traités par l’architecture WPD (Windows Portable Devices) :</span><span class="sxs-lookup"><span data-stu-id="2a784-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="2a784-105">Accès et stockage du contenu.</span><span class="sxs-lookup"><span data-stu-id="2a784-105">Accessing and storing content.</span></span> <span data-ttu-id="2a784-106">Par exemple, les applications doivent être en mesure d’ajouter des fichiers musicaux à un lecteur de musique portable.</span><span class="sxs-lookup"><span data-stu-id="2a784-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="2a784-107">Programmation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2a784-107">Programming the device.</span></span> <span data-ttu-id="2a784-108">Cela comprend des opérations simples telles que la modification des paramètres et la préparation de l’appareil pour la capture de données, ou des opérations plus complexes telles que le chargement du microprogramme.</span><span class="sxs-lookup"><span data-stu-id="2a784-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="2a784-109">Il peut s’agir par exemple de l’émission d’une commande « prendre une photo » sur un appareil photo encore numérique.</span><span class="sxs-lookup"><span data-stu-id="2a784-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="2a784-110">Dans WPD, ces comportements sont décrits en représentant l’appareil sous la forme d’une hiérarchie d’objets.</span><span class="sxs-lookup"><span data-stu-id="2a784-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="2a784-111">L’illustration suivante montre une représentation d’objet WPD pour un appareil à fonctions multiples, qui dans ce cas est un téléphone mobile.</span><span class="sxs-lookup"><span data-stu-id="2a784-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![Illustration montrant la hiérarchie des objets d’un téléphone mobile](images/wpd-overview-figure3.gif)

<span data-ttu-id="2a784-113">Cette hiérarchie illustre les fonctionnalités et le contenu suivants.</span><span class="sxs-lookup"><span data-stu-id="2a784-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="2a784-114">Ses</span><span class="sxs-lookup"><span data-stu-id="2a784-114">Functionality:</span></span>

-   <span data-ttu-id="2a784-115">Objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="2a784-115">Storage object.</span></span> <span data-ttu-id="2a784-116">Cet appareil a un stockage de données.</span><span class="sxs-lookup"><span data-stu-id="2a784-116">This device has data storage.</span></span>
-   <span data-ttu-id="2a784-117">Service de contacts.</span><span class="sxs-lookup"><span data-stu-id="2a784-117">Contacts Service.</span></span> <span data-ttu-id="2a784-118">Ce service est un objet fonctionnel qui peut être utilisé pour synchroniser et stocker des contacts sur le téléphone.</span><span class="sxs-lookup"><span data-stu-id="2a784-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="2a784-119">Service SMS.</span><span class="sxs-lookup"><span data-stu-id="2a784-119">SMS Service.</span></span> <span data-ttu-id="2a784-120">Ce service est un objet fonctionnel qui peut être utilisé pour envoyer, recevoir et stocker des messages SMS.</span><span class="sxs-lookup"><span data-stu-id="2a784-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="2a784-121">Contenu :</span><span class="sxs-lookup"><span data-stu-id="2a784-121">Contents:</span></span>

-   <span data-ttu-id="2a784-122">Objets multimédias.</span><span class="sxs-lookup"><span data-stu-id="2a784-122">Media objects.</span></span> <span data-ttu-id="2a784-123">Ce périphérique stocke des images, de la musique et des fichiers vidéo dans des dossiers sur l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="2a784-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="2a784-124">Tandis que les fichiers affichés dans l’illustration sont stockés dans un dossier, un appareil peut subdiviser le contenu en dossiers organisés selon le type de support stocké. par exemple, dossiers d’images, dossiers musicaux et dossiers vidéo.</span><span class="sxs-lookup"><span data-stu-id="2a784-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="2a784-125">Objets contact.</span><span class="sxs-lookup"><span data-stu-id="2a784-125">Contact objects.</span></span> <span data-ttu-id="2a784-126">Cet appareil stocke les informations de contact (telles que le nom, le numéro de téléphone et l’adresse) en tant qu’enfants du service de contacts.</span><span class="sxs-lookup"><span data-stu-id="2a784-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="2a784-127">Objets de message.</span><span class="sxs-lookup"><span data-stu-id="2a784-127">Message objects.</span></span> <span data-ttu-id="2a784-128">Cet appareil stocke les messages SMS en tant qu’enfants du service SMS.</span><span class="sxs-lookup"><span data-stu-id="2a784-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a784-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a784-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a784-130">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="2a784-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 




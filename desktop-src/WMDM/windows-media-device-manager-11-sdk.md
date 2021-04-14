---
title: Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11
description: Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Gestionnaire de périphériques Windows Media, à propos de
- Gestionnaire de périphériques, à propos de
- Protocole MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- Classe de stockage de masse (MSC)
- MSC (classe de stockage de masse)
- Windows Media Gestionnaire de périphériques, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- applications de bureau, à propos de
- Gestionnaire de périphériques Windows Media, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- fournisseurs de services, à propos de
- Gestionnaire de périphériques Windows Media, plug-ins
- Gestionnaire de périphériques, plug-INSP
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383124"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="fedbc-118">Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques 11</span><span class="sxs-lookup"><span data-stu-id="fedbc-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fedbc-119">Les API Windows Media Gestionnaire de périphériques sont désormais incluses dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fedbc-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="fedbc-120">Aucun téléchargement supplémentaire du SDK n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fedbc-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="fedbc-121">Le kit de développement logiciel (SDK) Microsoft Windows Media Gestionnaire de périphériques vous permet de créer des applications de bureau et des composants qui peuvent communiquer avec des appareils mobiles connectés.</span><span class="sxs-lookup"><span data-stu-id="fedbc-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="fedbc-122">Windows Media Gestionnaire de périphériques permet à votre application ou composant d’énumérer, d’explorer et d’échanger des fichiers avec un appareil, de rechercher des métadonnées et de demander des informations sur le nombre de jeux.</span><span class="sxs-lookup"><span data-stu-id="fedbc-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="fedbc-123">Les applications ou composants basés sur Windows Media Gestionnaire de périphériques ont une API cohérente pour communiquer avec un large éventail d’appareils, notamment le protocole MTP (Media Transfer Protocol), la classe de stockage de masse (MSC), l’RAPI et d’autres périphériques basés sur les versions les plus récentes et les plus anciennes de la technologie Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fedbc-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="fedbc-124">Vous pouvez créer les éléments suivants à l’aide du kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media :</span><span class="sxs-lookup"><span data-stu-id="fedbc-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="fedbc-125">Applications de bureau, telles que des lecteurs multimédias personnalisés.</span><span class="sxs-lookup"><span data-stu-id="fedbc-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="fedbc-126">Toutes les communications entre une application et un appareil mobile doivent traverser Windows Media Gestionnaire de périphériques, qui agit en tant que service Broker entre l’application, le système de gestion des droits numériques Microsoft et le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="fedbc-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="fedbc-127">Fournisseurs de services, qui jouent le rôle de lien de communication entre un appareil personnalisé et une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="fedbc-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="fedbc-128">Bien que Microsoft fournisse un certain nombre de fournisseurs de services qui peuvent communiquer avec la plupart des appareils prêts à l’emploi, vous pouvez créer un fournisseur de services personnalisé pour personnaliser la communication entre un appareil et une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="fedbc-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="fedbc-129">Des plug-ins, qui peuvent effectuer des tâches telles que la demande et la journalisation des nombres de lecture sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="fedbc-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="fedbc-130">Ces plug-ins peuvent être joints à d’autres applications de bureau, telles que le lecteur Windows Media, pour envoyer des informations aux fournisseurs de contenu afin de gérer les paiements de droits d’auteur.</span><span class="sxs-lookup"><span data-stu-id="fedbc-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="fedbc-131">Pour télécharger le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques, consultez [la page de téléchargement Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) sur le site Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="fedbc-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="fedbc-132">Ce kit de développement logiciel (SDK) est un composant du kit de développement logiciel (SDK) Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fedbc-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="fedbc-133">Les autres composants incluent le SDK Windows Media format, le kit de développement logiciel (SDK) Windows Media Services, le SDK Windows Media Encoder, le kit de développement logiciel (SDK) Windows Media Rights Manager et le kit de développement logiciel (SDK) Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="fedbc-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="fedbc-134">Cette documentation contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="fedbc-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="fedbc-135">Section</span><span class="sxs-lookup"><span data-stu-id="fedbc-135">Section</span></span>                                            | <span data-ttu-id="fedbc-136">Description</span><span class="sxs-lookup"><span data-stu-id="fedbc-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fedbc-137">Prise en main</span><span class="sxs-lookup"><span data-stu-id="fedbc-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="fedbc-138">Décrit les nouveautés de cette version de Windows Media Gestionnaire de périphériques, offre une vue d’ensemble du fonctionnement de Windows Media Gestionnaire de périphériques, décrit les éléments nécessaires au développement d’une application ou d’un fournisseur de services, et décrit les exemples fournis avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="fedbc-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="fedbc-139">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="fedbc-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="fedbc-140">Explique comment créer des applications et des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="fedbc-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="fedbc-141">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="fedbc-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="fedbc-142">Fournit des informations de référence sur C++ pour les interfaces, les méthodes, les classes et les structures prises en charge par le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fedbc-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="fedbc-143">*Glossaire*</span><span class="sxs-lookup"><span data-stu-id="fedbc-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="fedbc-144">Définit les termes utilisés dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="fedbc-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 





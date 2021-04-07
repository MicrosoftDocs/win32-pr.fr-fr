---
title: Avantages de l’utilisation de SIS
description: Les avantages de l’utilisation de SIS et de l’architecture de sauvegarde SIS sont les suivants.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Sauvegarde SIS (Single-Instance Store), avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028665"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="ff4ae-104">Avantages de l’utilisation de SIS</span><span class="sxs-lookup"><span data-stu-id="ff4ae-104">Advantages of Using SIS</span></span>

<span data-ttu-id="ff4ae-105">L’utilisation de SIS et l’architecture de sauvegarde SIS présentent les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="ff4ae-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="ff4ae-106">Les connexions entre les liaisons SIS et les fichiers de sauvegarde sont gérées automatiquement par l’architecture SIS lorsque vos applications de sauvegarde appellent les fonctions de l’API de sauvegarde SIS.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="ff4ae-107">Le contenu des points d’analyse SIS est opaque pour vos applications de sauvegarde et de restauration, ce qui garantit que les mises à niveau vers les éléments internes SIS ne nécessitent pas de modification de l’API SIS ou de vos applications de sauvegarde et de restauration qui appellent les fonctions API SIS.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="ff4ae-108">Vous devez uniquement recompiler votre application avec une nouvelle version de la DLL SIS, nommée Sisbkup.dll.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="ff4ae-109">Étant donné que SIS est implémenté en tant que pilote de filtre de système de fichiers, il suit en permanence les connexions entre les liens SIS et les fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="ff4ae-110">Une fois les fichiers sauvegardés et restaurés, la sauvegarde SIS garantit qu’une seule instance du fichier de sauvegarde sera sauvegardée et restaurée, quel que soit le nombre de liens SIS qui pointent vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ff4ae-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 





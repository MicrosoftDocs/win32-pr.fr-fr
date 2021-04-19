---
title: Suivi des plages modifiées d’un fichier
description: Suivi des plages modifiées d’un fichier
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106509883"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="75c5f-103">Suivi des plages modifiées d’un fichier</span><span class="sxs-lookup"><span data-stu-id="75c5f-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="75c5f-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="75c5f-104">Platforms</span></span>

<span data-ttu-id="75c5f-105">**Clients-** Windows 8.1 (toutes les références SKU)</span><span class="sxs-lookup"><span data-stu-id="75c5f-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="75c5f-106">**Serveurs-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="75c5f-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="75c5f-107">Description</span><span class="sxs-lookup"><span data-stu-id="75c5f-107">Description</span></span>

<span data-ttu-id="75c5f-108">L’équipe du système de fichiers NT (NTFS) a ajouté une nouvelle fonctionnalité à Windows.</span><span class="sxs-lookup"><span data-stu-id="75c5f-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="75c5f-109">Le journal USN génère un enregistrement de numéro de séquence de mise à jour (USN) contenant des plages modifiées pour un fichier lors de la fermeture.</span><span class="sxs-lookup"><span data-stu-id="75c5f-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="75c5f-110">Un nouveau type d’enregistrement, l' \_ enregistrement USN \_ v4 a été introduit pour enregistrer ces plages modifiées d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="75c5f-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="75c5f-111">La fonctionnalité n’est pas activée par défaut ; les utilisateurs doivent appeler une commande de contrôle de système de fichiers (FSCTL) pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="75c5f-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="75c5f-112">Toutefois, étant donné que d’autres composants Windows peuvent activer le suivi des plages, les utilisateurs et les développeurs peuvent percevoir que la fonctionnalité est toujours activée.</span><span class="sxs-lookup"><span data-stu-id="75c5f-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="75c5f-113">Windows permettra aux développeurs d’interroger le journal USN pour déterminer si le suivi des plages est activé.</span><span class="sxs-lookup"><span data-stu-id="75c5f-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="75c5f-114">La documentation MSDN sera fournie à une date ultérieure pour indiquer aux développeurs comment accéder aux \_ enregistrements v4 de l’enregistrement USN \_ .</span><span class="sxs-lookup"><span data-stu-id="75c5f-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="75c5f-115">Manifestation</span><span class="sxs-lookup"><span data-stu-id="75c5f-115">Manifestation</span></span>

<span data-ttu-id="75c5f-116">Toutes les applications existantes qui utilisent le journal USN continuent de fonctionner correctement, sans aucun problème de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="75c5f-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 





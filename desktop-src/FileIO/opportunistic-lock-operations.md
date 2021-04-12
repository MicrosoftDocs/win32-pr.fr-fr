---
description: Si une application demande des verrous opportunistes, tous les fichiers pour lesquels elle demande des verrous doivent être ouverts pour les entrées et sorties avec chevauchement (asynchrone) à l’aide de la fonction CreateFile avec l’indicateur de CHEVAUCHement de l’indicateur de fichier \_ \_ .
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: Opérations de verrouillage opportuniste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529139"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="fc70e-103">Opérations de verrouillage opportuniste</span><span class="sxs-lookup"><span data-stu-id="fc70e-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="fc70e-104">Si une application demande des verrous opportunistes, tous les fichiers pour lesquels elle demande des verrous doivent être ouverts pour les entrées et sorties avec chevauchement (asynchrone) à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier.</span><span class="sxs-lookup"><span data-stu-id="fc70e-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="fc70e-105">Une fois les fichiers ouverts pour une opération avec chevauchement, vous pouvez utiliser la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec l’un des codes de contrôle suivants pour travailler avec ces fichiers «verrous opportunistes :</span><span class="sxs-lookup"><span data-stu-id="fc70e-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="fc70e-106">**fermeture de l’accusé de réception FSCTL \_ OPBATCH \_ \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="fc70e-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="fc70e-107">**FSCTL de \_ rupture de verrou OPLOCK \_ \_ \_ non \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fc70e-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="fc70e-108">**\_accusé de réception FSCTL OPLOCK \_ break \_**</span><span class="sxs-lookup"><span data-stu-id="fc70e-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="fc70e-109">**\_notification de \_ rupture \_ OPLOCK FSCTL**</span><span class="sxs-lookup"><span data-stu-id="fc70e-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="fc70e-110">**\_ \_ OPLOCK batch de demande FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="fc70e-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="fc70e-111">**\_ \_ OPLOCK filtre de requête FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="fc70e-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="fc70e-112">**\_OPLOCK Request \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="fc70e-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="fc70e-113">**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fc70e-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="fc70e-114">**FSCTL \_ demande \_ OPLOCK \_ niveau \_ 2**</span><span class="sxs-lookup"><span data-stu-id="fc70e-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 

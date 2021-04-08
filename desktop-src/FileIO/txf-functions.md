---
description: Fonctions NTFS (TxF) transactionnelles.
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Fonctions TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758830"
---
# <a name="txf-functions"></a><span data-ttu-id="c5b8c-103">Fonctions TxF</span><span class="sxs-lookup"><span data-stu-id="c5b8c-103">TxF Functions</span></span>

<span data-ttu-id="c5b8c-104">NTFS transactionnel (TxF) fournit les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5b8c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c5b8c-105">In this section</span></span>



| <span data-ttu-id="c5b8c-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="c5b8c-106">Function</span></span>                                                                      | <span data-ttu-id="c5b8c-107">Description</span><span class="sxs-lookup"><span data-stu-id="c5b8c-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5b8c-108">**TxfLogCreateFileReadContext**</span><span class="sxs-lookup"><span data-stu-id="c5b8c-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="c5b8c-109">Crée un contexte à utiliser pour lire les enregistrements de réplication.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="c5b8c-110">**TxfLogDestroyReadContext**</span><span class="sxs-lookup"><span data-stu-id="c5b8c-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="c5b8c-111">Ferme un contexte de lecture créé par la fonction [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .</span><span class="sxs-lookup"><span data-stu-id="c5b8c-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="c5b8c-112">**TxfLogReadRecords**</span><span class="sxs-lookup"><span data-stu-id="c5b8c-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="c5b8c-113">Lit les enregistrements de restauration par progression dans le journal.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 





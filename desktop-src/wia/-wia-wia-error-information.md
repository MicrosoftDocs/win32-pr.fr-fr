---
description: Les API WIA (Windows Image Acquisition) renvoient leur état d’achèvement dans une valeur de retour HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informations sur l’erreur WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516264"
---
# <a name="wia-error-information"></a><span data-ttu-id="cf629-103">Informations sur l’erreur WIA</span><span class="sxs-lookup"><span data-stu-id="cf629-103">WIA Error Information</span></span>

<span data-ttu-id="cf629-104">Les API WIA (Windows Image Acquisition) renvoient leur état d’achèvement dans une valeur de retour HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cf629-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="cf629-105">Les applications vérifient ces valeurs de retour par rapport à la constante d’installation \_ WIA pour déterminer si l’erreur nécessite une intervention de l’utilisateur, telle qu’un bourrage papier, et les signaler à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf629-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="cf629-106">En outre, toutes les erreurs au niveau du pilote sont consignées en détail dans le journal des événements, à l’aide des chaînes d’erreur fournies par le minipilote d’appareil.</span><span class="sxs-lookup"><span data-stu-id="cf629-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="cf629-107">Pour obtenir la liste des codes d’erreur spécifiques à WIA, consultez [codes d’erreur](-wia-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cf629-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 




---
title: Handle de fuite D1103
ms.assetid: 9bb08cd6-104a-4168-b14e-3caec1679388
description: Une interface a été créée mais n’a pas été libérée.
keywords:
- D1103 de descripteur Direct2D perdue
topic_type:
- apiref
api_name:
- D1103 Leaked Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cc4b4e43f94bd4ceb5d7a2518879c69bd3ecf8f3
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106531173"
---
# <a name="d1103-leaked-handle"></a><span data-ttu-id="5c190-104">D1103 : handle divulgué</span><span class="sxs-lookup"><span data-stu-id="5c190-104">D1103: Leaked Handle</span></span>

<span data-ttu-id="5c190-105">Une interface d’interface \[  \] a été créée mais n’a pas été libérée.</span><span class="sxs-lookup"><span data-stu-id="5c190-105">An interface \[*interface*\] was created but not released.</span></span>

## <a name="placeholders"></a><span data-ttu-id="5c190-106">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="5c190-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="5c190-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="5c190-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="5c190-108">Adresse de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5c190-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="5c190-109">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="5c190-109">Possible Causes</span></span>

<span data-ttu-id="5c190-110">Utilisation des ressources non valide.</span><span class="sxs-lookup"><span data-stu-id="5c190-110">Invalid resource usage.</span></span> <span data-ttu-id="5c190-111">Une application ne peut pas libérer une interface lorsqu’elle n’est plus utilisée.</span><span class="sxs-lookup"><span data-stu-id="5c190-111">An application fails to release an interface when it is no longer in use.</span></span>

 

 





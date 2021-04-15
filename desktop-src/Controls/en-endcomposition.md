---
title: Code de notification EN_ENDCOMPOSITION (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur a entré de nouvelles données ou a fini d’entrer des données lors de l’utilisation de l’éditeur IME ou Text Services Framework.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Contrôles Windows de code de notification EN_ENDCOMPOSITION
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464423"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="367a1-104">\_Code de notification en ENDCOMPOSITION</span><span class="sxs-lookup"><span data-stu-id="367a1-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="367a1-105">Avertit une fenêtre parente du contrôle RichEdit que l’utilisateur a entré de nouvelles données ou a fini d’entrer des données lors de l’utilisation de l’éditeur IME ou [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="367a1-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="367a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="367a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367a1-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="367a1-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="367a1-108">Structure [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) qui reçoit des informations sur la condition de fin de composition.</span><span class="sxs-lookup"><span data-stu-id="367a1-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="367a1-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="367a1-109">Requirements</span></span>



| <span data-ttu-id="367a1-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="367a1-110">Requirement</span></span> | <span data-ttu-id="367a1-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="367a1-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="367a1-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="367a1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="367a1-113">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="367a1-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="367a1-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="367a1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="367a1-115">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="367a1-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="367a1-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="367a1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="367a1-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="367a1-117"><dt>Richedit.h</dt></span></span> </dl> |



 


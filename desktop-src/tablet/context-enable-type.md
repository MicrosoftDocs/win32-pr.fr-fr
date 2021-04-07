---
description: Indique si les messages de contexte doivent être envoyés à la procédure de fenêtre de la fenêtre propriétaire.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Énumération CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758854"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="0450d-103">\_Énumération des types d’activation de contexte \_</span><span class="sxs-lookup"><span data-stu-id="0450d-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="0450d-104">Indique si les messages de contexte doivent être envoyés à la procédure de fenêtre de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="0450d-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0450d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0450d-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="0450d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0450d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0450d-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**activation du contexte \_**</span><span class="sxs-lookup"><span data-stu-id="0450d-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0450d-108">Le contexte de tablette doit être activé, ce qui entraîne l’envoi de messages de contexte à la procédure de fenêtre de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="0450d-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0450d-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**désactiver le contexte \_**</span><span class="sxs-lookup"><span data-stu-id="0450d-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0450d-110">Le contexte de tablette doit être désactivé, ce qui empêche tout autre message de contexte d’être envoyé à la procédure de fenêtre ou au récepteur d’événements de la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="0450d-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0450d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0450d-111">Requirements</span></span>



| <span data-ttu-id="0450d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0450d-112">Requirement</span></span> | <span data-ttu-id="0450d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0450d-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0450d-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0450d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0450d-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0450d-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0450d-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0450d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0450d-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0450d-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="0450d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0450d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0450d-119">**ITablet :: CreateContext, méthode**</span><span class="sxs-lookup"><span data-stu-id="0450d-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 





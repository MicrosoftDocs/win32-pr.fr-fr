---
title: Message MMIOM_CLOSE (mmsystem. h)
description: Le \_ message MMIOM Close est envoyé à une procédure d’e/s par la fonction mmioClose pour demander la fermeture d’un fichier.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Message MMIOM_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519297"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="0e271-104">MMIOM \_ Fermer le message</span><span class="sxs-lookup"><span data-stu-id="0e271-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="0e271-105">Le message **MMIOM \_ Close** est envoyé à une procédure d’e/s par la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) pour demander la fermeture d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0e271-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0e271-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e271-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span><span class="sxs-lookup"><span data-stu-id="0e271-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0e271-108">Indicateurs contenus dans le paramètre **wFlags** de **mmioClose**.</span><span class="sxs-lookup"><span data-stu-id="0e271-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e271-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0e271-109">Return Value</span></span>

<span data-ttu-id="0e271-110">Retourne zéro si le fichier est fermé avec succès ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0e271-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e271-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e271-111">Requirements</span></span>



| <span data-ttu-id="0e271-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e271-112">Requirement</span></span> | <span data-ttu-id="0e271-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e271-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e271-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e271-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0e271-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e271-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e271-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e271-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0e271-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e271-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e271-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e271-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e271-119"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e271-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


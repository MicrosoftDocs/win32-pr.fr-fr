---
description: Envoie un message au contrôle spécifié dans une boîte de dialogue.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535891"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="1e66b-103">\_SendDlgItemMessage fonction)</span><span class="sxs-lookup"><span data-stu-id="1e66b-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="1e66b-104">\[Cette fonction est un wrapper sur la fonction **SendDlgItemMessage** .</span><span class="sxs-lookup"><span data-stu-id="1e66b-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="1e66b-105">Cette fonction peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="1e66b-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="1e66b-106">Les applications doivent appeler **SendDlgItemMessage** directement.\]</span><span class="sxs-lookup"><span data-stu-id="1e66b-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="1e66b-107">Envoie un message au contrôle spécifié dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1e66b-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="1e66b-108">Consultez [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="1e66b-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e66b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e66b-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="1e66b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e66b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e66b-111">*...*</span><span class="sxs-lookup"><span data-stu-id="1e66b-111">*...*</span></span> 
<span data-ttu-id="1e66b-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e66b-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1e66b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e66b-113">Requirements</span></span>



| <span data-ttu-id="1e66b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e66b-114">Requirement</span></span> | <span data-ttu-id="1e66b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e66b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e66b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1e66b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1e66b-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e66b-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e66b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e66b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e66b-119">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="1e66b-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 

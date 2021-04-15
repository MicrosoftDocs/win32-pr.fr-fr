---
title: Message WM_COPYDATA (winuser. h)
description: Une application envoie le \_ message WM COPYDATA pour passer des données à une autre application.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA l’échange de données de message
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465615"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="955f0-104">\_Message WM COPYDATA</span><span class="sxs-lookup"><span data-stu-id="955f0-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="955f0-105">Une application envoie le message **WM \_ COPYDATA** pour passer des données à une autre application.</span><span class="sxs-lookup"><span data-stu-id="955f0-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="955f0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="955f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="955f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="955f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="955f0-108">Handle de la fenêtre qui passe les données.</span><span class="sxs-lookup"><span data-stu-id="955f0-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="955f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="955f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="955f0-110">Pointeur vers une structure [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) qui contient les données à passer.</span><span class="sxs-lookup"><span data-stu-id="955f0-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="955f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="955f0-111">Return value</span></span>

<span data-ttu-id="955f0-112">Si l’application réceptrice traite ce message, elle doit retourner la **valeur true**; Sinon, elle doit retourner **false**.</span><span class="sxs-lookup"><span data-stu-id="955f0-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="955f0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="955f0-113">Remarks</span></span>

<span data-ttu-id="955f0-114">Les données transmises ne doivent pas contenir de pointeurs ou d’autres références à des objets qui ne sont pas accessibles à l’application recevant les données.</span><span class="sxs-lookup"><span data-stu-id="955f0-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="955f0-115">Pendant l’envoi de ce message, les données référencées ne doivent pas être modifiées par un autre thread du processus d’envoi.</span><span class="sxs-lookup"><span data-stu-id="955f0-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="955f0-116">L’application réceptrice doit tenir compte des données en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="955f0-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="955f0-117">Le paramètre *lParam* n’est valide que pendant le traitement du message.</span><span class="sxs-lookup"><span data-stu-id="955f0-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="955f0-118">L’application réceptrice ne doit pas libérer la mémoire référencée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="955f0-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="955f0-119">Si l’application réceptrice doit accéder aux données après que [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) a été retourné, elle doit copier les données dans une mémoire tampon locale.</span><span class="sxs-lookup"><span data-stu-id="955f0-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="955f0-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="955f0-120">Examples</span></span>

<span data-ttu-id="955f0-121">Pour obtenir un exemple, consultez Utilisation de la [copie de données](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="955f0-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="955f0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="955f0-122">Requirements</span></span>



| <span data-ttu-id="955f0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="955f0-123">Requirement</span></span> | <span data-ttu-id="955f0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="955f0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955f0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="955f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="955f0-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="955f0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="955f0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="955f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="955f0-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="955f0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="955f0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="955f0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="955f0-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="955f0-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955f0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="955f0-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="955f0-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="955f0-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="955f0-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="955f0-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="955f0-134">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="955f0-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 


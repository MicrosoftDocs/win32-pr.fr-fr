---
description: Avertit une application lorsque l’IME sélectionné a besoin de la chaîne convertie à partir de l’application. L’application reçoit cette commande via le \_ message de \_ demande de l’IME WM avec les paramètres définis comme indiqué ci-dessous.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED le code de notification (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202760"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="c5ee5-104">\_Code de notification IMR DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="c5ee5-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="c5ee5-105">Avertit une application lorsque l’IME sélectionné a besoin de la chaîne convertie à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="c5ee5-106">L’application reçoit cette commande via le message de [**\_ \_ demande de l’IME WM**](wm-ime-request.md) avec les paramètres définis comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="c5ee5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5ee5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ee5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5ee5-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="c5ee5-109">Définissez sur IMR \_ DOCUMENTFEED.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="c5ee5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5ee5-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="c5ee5-111">Pointeur vers une mémoire tampon destinée à contenir la structure [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="c5ee5-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ee5-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c5ee5-112">Return Value</span></span>

<span data-ttu-id="c5ee5-113">Retourne la structure actuelle de la chaîne de reconversion.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="c5ee5-114">Si *lParam* a la valeur **null**, l’application retourne la taille requise pour que la mémoire tampon contienne la structure.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="c5ee5-115">La commande retourne 0 en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ee5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c5ee5-116">Remarks</span></span>

<span data-ttu-id="c5ee5-117">L’IME met en cache les chaînes converties pour une meilleure précision de conversion.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="c5ee5-118">L’une des limitations de mise en cache de l’IME est qu’elle perd la chaîne convertie dans les circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5ee5-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="c5ee5-119">La position du signe insertion de l’application est déplacée par une clé, par exemple, une clé de curseur.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="c5ee5-120">La position du signe insertion de l’application est déplacée par la souris.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="c5ee5-121">Un nouveau document est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-121">A new document is opened.</span></span>

<span data-ttu-id="c5ee5-122">Avec la commande **IMR \_ DOCUMENTFEED** , l’IME peut actualiser ses chaînes mises en cache à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="c5ee5-123">L’utilisation de cette commande améliore la précision de la conversion.</span><span class="sxs-lookup"><span data-stu-id="c5ee5-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ee5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5ee5-124">Requirements</span></span>



| <span data-ttu-id="c5ee5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5ee5-125">Requirement</span></span> | <span data-ttu-id="c5ee5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5ee5-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ee5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5ee5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ee5-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5ee5-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5ee5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5ee5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ee5-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5ee5-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c5ee5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5ee5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ee5-132"><dt>IMM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5ee5-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ee5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5ee5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ee5-134">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="c5ee5-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="c5ee5-135">Commandes du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="c5ee5-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="c5ee5-136">**RECONVERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="c5ee5-137">**demande de l' \_ IME WM \_**</span><span class="sxs-lookup"><span data-stu-id="c5ee5-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 





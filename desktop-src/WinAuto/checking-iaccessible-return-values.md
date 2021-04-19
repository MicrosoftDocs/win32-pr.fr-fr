---
title: Vérification des valeurs de retour IAccessible
description: Les développeurs clients ne doivent pas s’appuyer sur les macros COM (Component Object Model) ayant réussi et n’ont pas réussi à tester les valeurs de retour IAccessible, car les valeurs autres que \_ OK sont considérées comme ayant réussi.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510485"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="16da4-103">Vérification des valeurs de retour IAccessible</span><span class="sxs-lookup"><span data-stu-id="16da4-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="16da4-104">Les développeurs clients ne doivent pas s’appuyer sur les macros COM (Component Object Model) ayant [**réussi**](/windows/desktop/api/winerror/nf-winerror-succeeded) et [**n’ont pas**](/windows/desktop/api/winerror/nf-winerror-failed) réussi à tester les valeurs de retour [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , car les valeurs autres que \_ OK sont considérées comme ayant réussi.</span><span class="sxs-lookup"><span data-stu-id="16da4-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="16da4-105">Par exemple, une méthode peut retourner \_ la valeur S false, qui est considérée comme un succès par la macro **Succeeded** , mais qui reçoit toujours un pointeur **null** dans un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="16da4-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="16da4-106">Les développeurs clients doivent se prémunir contre la possibilité que certains serveurs retournent des codes d’erreur autres que les valeurs documentées.</span><span class="sxs-lookup"><span data-stu-id="16da4-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="16da4-107">Pour être sûr, vous devez vous assurer que tous les paramètres de sortie contiennent des informations valides et répondent aux critères suivants :</span><span class="sxs-lookup"><span data-stu-id="16da4-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="16da4-108">Tous les pointeurs ne sont pas **null**.</span><span class="sxs-lookup"><span data-stu-id="16da4-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="16da4-109">Le membre **VT** d’une structure [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) n’est pas égal à VT \_ vide.</span><span class="sxs-lookup"><span data-stu-id="16da4-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 
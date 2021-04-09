---
title: Gestion des erreurs des objets de service
description: Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel IDispatch Invoke doit être DISP \_ E \_ exception, et le pointeur de paramètre pExceptInfo vers une structure EXCEPTINFO dans le doit être renseigné.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101800"
---
# <a name="service-object-error-handling"></a><span data-ttu-id="5daa5-103">Gestion des erreurs des objets de service</span><span class="sxs-lookup"><span data-stu-id="5daa5-103">Service Object Error Handling</span></span>

<span data-ttu-id="5daa5-104">Lorsqu’une erreur se produit dans un objet de service, la valeur de retour de l’appel [**IDispatch :: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) doit être DISP \_ E \_ exception, et le pointeur de paramètre *pExceptInfo* vers une structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) dans le doit être renseigné.</span><span class="sxs-lookup"><span data-stu-id="5daa5-104">When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure in the should be filled in.</span></span>

<span data-ttu-id="5daa5-105">Plus précisément, les membres **bstrSource** et **bstrDescription** de la structure [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) sont utilisés par l’hôte d’appareil avec la technologie UPnP pour créer une réponse d’erreur UPnP. **bstrSource** est le code d’erreur et **bstrDescription** est la description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5daa5-105">Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.</span></span>

 

 
---
title: Présentation du client
description: Cette rubrique répertorie les façons dont un client affiche les données ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- les extensions ADSI, ce qu’un client voit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508129"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="8a2a5-104">Qu’est-ce qu’un client ?</span><span class="sxs-lookup"><span data-stu-id="8a2a5-104">What Does a Client See?</span></span>

-   <span data-ttu-id="8a2a5-105">Un client voit ADSI et tous ses objets d’extension comme un seul objet.</span><span class="sxs-lookup"><span data-stu-id="8a2a5-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="8a2a5-106">Un client ADSI voit une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui gère toutes les interfaces de dispatch et de double dans l’objet, que l’interface de dispatch ou double soit implémentée par l’agrégateur dans le fournisseur ou par une extension.</span><span class="sxs-lookup"><span data-stu-id="8a2a5-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="8a2a5-107">Consultez la [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8a2a5-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="8a2a5-108">ADSI n’expose aucune information de type par le biais des méthodes [**IDispatch :: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ou [**IDispatch :: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) .</span><span class="sxs-lookup"><span data-stu-id="8a2a5-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="8a2a5-109">ADSI fournit des informations de type par le biais de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="8a2a5-109">ADSI provides type information through the type library.</span></span>

 

 
---
title: Interfaces doubles (ADSI)
description: Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730188"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="3c054-103">Interfaces doubles (ADSI)</span><span class="sxs-lookup"><span data-stu-id="3c054-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="3c054-104">Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3c054-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="3c054-105">Une propriété en lecture seule est mappée à une entrée d’interface de la forme **obtenir \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="3c054-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="3c054-106">Une propriété en lecture/écriture mappe à deux entrées d’interface de la forme **obtenir \_ <PropertyName>** et **Placer \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="3c054-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="3c054-107">Toutes les méthodes sur une interface COM doivent :</span><span class="sxs-lookup"><span data-stu-id="3c054-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="3c054-108">Retourne une valeur HRESULT pour indiquer la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="3c054-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="3c054-109">Le type **HRESULT** est abordé dans la spécification com.</span><span class="sxs-lookup"><span data-stu-id="3c054-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="3c054-110">Lors des appels à **QueryInterface**, retournez **E \_ nointerface** pour les interfaces non implémentées.</span><span class="sxs-lookup"><span data-stu-id="3c054-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="3c054-111">Retournez **E \_ NOTIMPL** pour les méthodes non implémentées sur les interfaces implémentées autrement.</span><span class="sxs-lookup"><span data-stu-id="3c054-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="3c054-112">Renvoie **la \_ propriété E ADS \_ \_ non \_ prise en charge** pour les propriétés d’interface qui ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3c054-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="3c054-113">Pour conserver la compatibilité avec les contrôleurs Automation, tous les paramètres et types de retour doivent se trouver dans le sous-ensemble défini par le type de données Automation VARIANT.</span><span class="sxs-lookup"><span data-stu-id="3c054-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="3c054-114">Pour plus d’informations, consultez **Variant** et **VARIANTARG** dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="3c054-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="3c054-115">Un objet Active Directory fournisseur peut exposer des interfaces qui utilisent des types de données autres que ceux du sous-ensemble **Variant** .</span><span class="sxs-lookup"><span data-stu-id="3c054-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="3c054-116">Toutefois, les contrôleurs Automation tels que les Visual Basic ne sont pas en mesure d’appeler ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="3c054-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="3c054-117">La plupart des interfaces de fournisseur ADSI sont dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et peuvent être utilisées comme pointeurs d’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="3c054-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="3c054-118">Toutefois, les interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)et [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ne sont pas dérivées de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="3c054-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 
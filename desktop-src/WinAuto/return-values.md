---
title: Valeurs de retour (fonctionnalités d’accessibilité Windows)
description: Cette rubrique décrit les valeurs de retour les plus courantes et les autres valeurs de retour que vous pouvez voir moins fréquemment.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464011"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="99e1d-103">Valeurs de retour (fonctionnalités d’accessibilité Windows)</span><span class="sxs-lookup"><span data-stu-id="99e1d-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="99e1d-104">Cette rubrique décrit les valeurs de retour les plus courantes et les autres valeurs de retour que vous pouvez voir moins fréquemment.</span><span class="sxs-lookup"><span data-stu-id="99e1d-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="99e1d-105">Valeurs de retour courantes</span><span class="sxs-lookup"><span data-stu-id="99e1d-105">Common Return Values</span></span>

<span data-ttu-id="99e1d-106">Les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retournent l’une des valeurs suivantes, définies dans Winerror. h, ou un autre code d’erreur com (Component Object Model) standard :</span><span class="sxs-lookup"><span data-stu-id="99e1d-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e1d-107">\_OK</span><span class="sxs-lookup"><span data-stu-id="99e1d-107">S\_OK</span></span>                   | <span data-ttu-id="99e1d-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="99e1d-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="99e1d-109">S \_ false</span><span class="sxs-lookup"><span data-stu-id="99e1d-109">S\_FALSE</span></span>                | <span data-ttu-id="99e1d-110">La méthode a réussi en partie.</span><span class="sxs-lookup"><span data-stu-id="99e1d-110">The method succeeded in part.</span></span> <span data-ttu-id="99e1d-111">Cela se produit lorsque la méthode est réussie, mais que les informations demandées ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="99e1d-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="99e1d-112">Par exemple, Microsoft Active Accessibility retourne S \_ false si vous appelez [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) pour récupérer un objet enfant à un point donné et que le point spécifié ne se trouve pas dans l’objet ou l’enfant de l’objet.</span><span class="sxs-lookup"><span data-stu-id="99e1d-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="99e1d-113">\_MEMBERNOTFOUND DISP \_</span><span class="sxs-lookup"><span data-stu-id="99e1d-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="99e1d-114">L’objet ne prend pas en charge la propriété ou l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="99e1d-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="99e1d-115">Par exemple, un bouton de commande retourne cette valeur si vous demandez sa [propriété Value](value-property.md), car elle ne possède pas de propriété Value.</span><span class="sxs-lookup"><span data-stu-id="99e1d-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="99e1d-116">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="99e1d-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="99e1d-117">Cette méthode n'est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="99e1d-117">The method is not implemented.</span></span> <span data-ttu-id="99e1d-118">Cette valeur se produit lorsqu’un client appelle une méthode qui n’est pas encore prise en charge dans ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="99e1d-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="99e1d-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="99e1d-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="99e1d-120">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="99e1d-120">One or more arguments were not valid.</span></span> <span data-ttu-id="99e1d-121">Cette erreur se produit lorsque l’appelant tente d’identifier un objet enfant à l’aide d’un identificateur que le serveur ne reconnaît pas.</span><span class="sxs-lookup"><span data-stu-id="99e1d-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="99e1d-122">Cette erreur se produit également lorsqu’un client tente d’identifier un objet enfant dans un objet qui n’a pas d’enfants.</span><span class="sxs-lookup"><span data-stu-id="99e1d-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="99e1d-123">\_OUTOFMEMORY E</span><span class="sxs-lookup"><span data-stu-id="99e1d-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="99e1d-124">La méthode n’a pas pu allouer de la mémoire requise pour terminer une opération cruciale pour sa réussite.</span><span class="sxs-lookup"><span data-stu-id="99e1d-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="99e1d-125">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="99e1d-125">E\_FAIL</span></span>                 | <span data-ttu-id="99e1d-126">Une erreur inconnue ou générique s’est produite.</span><span class="sxs-lookup"><span data-stu-id="99e1d-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="99e1d-127">Valeurs de retour supplémentaires</span><span class="sxs-lookup"><span data-stu-id="99e1d-127">Additional Return Values</span></span>

<span data-ttu-id="99e1d-128">Les valeurs de retour suivantes peuvent être retournées par les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="99e1d-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="99e1d-129">Ces valeurs de retour ne sont pas aussi courantes que les valeurs précédentes, mais vous devez en être conscient.</span><span class="sxs-lookup"><span data-stu-id="99e1d-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99e1d-130">\_ACCESSDENIED E</span><span class="sxs-lookup"><span data-stu-id="99e1d-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="99e1d-131">Elle est retournée lorsque vous appelez \_ la commande obtenir accValue pour obtenir la valeur d’un contrôle de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="99e1d-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="99e1d-132">\_exception DISP E \_</span><span class="sxs-lookup"><span data-stu-id="99e1d-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="99e1d-133">CO \_ E \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="99e1d-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 





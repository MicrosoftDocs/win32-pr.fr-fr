---
title: Gestion des erreurs COM dans Java et Visual Basic
description: Gestion des erreurs COM dans Java et Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424009"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="e9fb2-103">Gestion des erreurs COM dans Java et Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e9fb2-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="e9fb2-104">Il existe trois interfaces et trois fonctions qui peuvent être utilisées dans COM pour assurer la gestion des erreurs lors de la programmation en Java ou Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="e9fb2-105">En Java et Visual Basic, l’appel de méthode ne retourne pas de valeur **HRESULT** comme valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="e9fb2-106">Au lieu de cela, ces langages utilisent les interfaces et les fonctions COM pour obtenir des valeurs **HRESULT** et pour gérer les erreurs ou les exceptions.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="e9fb2-107">(Les exceptions sont des événements qui se trouvent au-delà du contrôle du programme, tels que des problèmes de fichier ou des paramètres non valides.)</span><span class="sxs-lookup"><span data-stu-id="e9fb2-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="e9fb2-108">Les trois interfaces qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="e9fb2-109">Interface</span><span class="sxs-lookup"><span data-stu-id="e9fb2-109">Interface</span></span>                                                                        |  <span data-ttu-id="e9fb2-110">Description</span><span class="sxs-lookup"><span data-stu-id="e9fb2-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9fb2-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="e9fb2-112">Définit les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="e9fb2-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="e9fb2-114">Retourne des informations à partir d’un objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="e9fb2-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="e9fb2-116">Identifie l’objet comme prenant en charge l’interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="e9fb2-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="e9fb2-117">Les trois fonctions qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="e9fb2-118">Interface</span><span class="sxs-lookup"><span data-stu-id="e9fb2-118">Interface</span></span>       |       <span data-ttu-id="e9fb2-119">Description</span><span class="sxs-lookup"><span data-stu-id="e9fb2-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9fb2-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="e9fb2-121">Crée une instance d’un objet d’erreur générique.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e9fb2-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="e9fb2-123">Obtient le pointeur d’informations d’erreur défini par l’appel précédent à [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) dans le thread logique actuel.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="e9fb2-124">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e9fb2-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="e9fb2-125">Définit l’objet d’informations d’erreur pour le thread d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="e9fb2-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e9fb2-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e9fb2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9fb2-127">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="e9fb2-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 


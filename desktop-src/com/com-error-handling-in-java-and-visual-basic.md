---
title: Gestion des erreurs COM dans Java et Visual Basic
description: Gestion des erreurs COM dans Java et Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382963"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="dc9ff-103">Gestion des erreurs COM dans Java et Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dc9ff-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="dc9ff-104">Il existe trois interfaces et trois fonctions qui peuvent être utilisées dans COM pour assurer la gestion des erreurs lors de la programmation en Java ou Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="dc9ff-105">En Java et Visual Basic, l’appel de méthode ne retourne pas de valeur **HRESULT** comme valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="dc9ff-106">Au lieu de cela, ces langages utilisent les interfaces et les fonctions COM pour obtenir des valeurs **HRESULT** et pour gérer les erreurs ou les exceptions.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="dc9ff-107">(Les exceptions sont des événements qui se trouvent au-delà du contrôle du programme, tels que des problèmes de fichier ou des paramètres non valides.)</span><span class="sxs-lookup"><span data-stu-id="dc9ff-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="dc9ff-108">Les trois interfaces qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc9ff-109">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="dc9ff-110">Définit les informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="dc9ff-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="dc9ff-112">Retourne des informations à partir d’un objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="dc9ff-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="dc9ff-114">Identifie l’objet comme prenant en charge l’interface [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="dc9ff-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="dc9ff-115">Les trois fonctions qui assurent la prise en charge de **HRESULT** s sont répertoriées et décrites brièvement dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc9ff-116">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="dc9ff-117">Crée une instance d’un objet d’erreur générique.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="dc9ff-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="dc9ff-119">Obtient le pointeur d’informations d’erreur défini par l’appel précédent à [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) dans le thread logique actuel.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="dc9ff-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc9ff-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="dc9ff-121">Définit l’objet d’informations d’erreur pour le thread d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="dc9ff-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="dc9ff-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc9ff-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9ff-123">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="dc9ff-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 


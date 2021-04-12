---
title: Extraction des informations sur les erreurs
description: Extraction des informations sur les erreurs
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031887"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="81a24-103">Extraction des informations sur les erreurs</span><span class="sxs-lookup"><span data-stu-id="81a24-103">Retrieving Error Information</span></span>

<span data-ttu-id="81a24-104">À l’aide des interfaces et des fonctions de gestion des erreurs COM, vous pouvez récupérer les informations d’erreur comme suit :</span><span class="sxs-lookup"><span data-stu-id="81a24-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="81a24-105">Vérifiez si la valeur retournée représente une erreur que l’objet est prêt à gérer.</span><span class="sxs-lookup"><span data-stu-id="81a24-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="81a24-106">Appelez [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur vers l’interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="81a24-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="81a24-107">Appelez ensuite [**ISupportErrorInfo :: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) pour vérifier que l’erreur a été déclenchée par l’objet qui l’a retourné et que l’objet d’erreur se rapporte à l’erreur actuelle et non à un appel précédent.</span><span class="sxs-lookup"><span data-stu-id="81a24-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="81a24-108">Pour obtenir un pointeur vers l’objet d’erreur, appelez la fonction [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="81a24-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="81a24-109">Pour récupérer des informations de l’objet Error, utilisez les méthodes [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="81a24-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="81a24-110">Si l’objet n’est pas préparé à gérer l’erreur mais doit propager les informations d’erreur plus loin dans la chaîne d’appel, il doit simplement transmettre la valeur de retour à son appelant.</span><span class="sxs-lookup"><span data-stu-id="81a24-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="81a24-111">Étant donné que la fonction [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) efface les informations d’erreur et transmet la propriété de l’objet d’erreur à l’appelant, la fonction doit être appelée uniquement par l’objet qui gère l’erreur.</span><span class="sxs-lookup"><span data-stu-id="81a24-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 
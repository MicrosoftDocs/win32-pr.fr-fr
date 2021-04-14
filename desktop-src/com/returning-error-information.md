---
title: Retour d’informations sur l’erreur
description: Retour d’informations sur l’erreur
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382915"
---
# <a name="returning-error-information"></a><span data-ttu-id="10af6-103">Retour d’informations sur l’erreur</span><span class="sxs-lookup"><span data-stu-id="10af6-103">Returning Error Information</span></span>

<span data-ttu-id="10af6-104">À l’aide des interfaces et des fonctions de gestion des erreurs COM, vous pouvez retourner des informations sur les erreurs en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="10af6-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="10af6-105">Implémentez l’interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="10af6-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="10af6-106">Pour créer une instance de l’objet d’erreur générique, appelez la fonction [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="10af6-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="10af6-107">Pour définir son contenu, utilisez les méthodes [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="10af6-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="10af6-108">Pour associer l’objet d’erreur au thread logique actuel, appelez la fonction [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="10af6-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="10af6-109">Les interfaces de gestion des erreurs créent et gèrent un objet d’erreur qui fournit des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="10af6-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="10af6-110">L’objet d’erreur n’est pas le même que l’objet qui a rencontré l’erreur.</span><span class="sxs-lookup"><span data-stu-id="10af6-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="10af6-111">Il s’agit d’un objet distinct associé au thread d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="10af6-111">It is a separate object associated with the current thread of execution.</span></span>

 

 
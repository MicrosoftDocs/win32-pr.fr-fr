---
description: Les modules de sortie personnalisés doivent implémenter l’interface ICertExit, qui est appelée par le moteur serveur.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Écriture de modules de sortie personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541228"
---
# <a name="writing-custom-exit-modules"></a><span data-ttu-id="4c451-103">Écriture de modules de sortie personnalisés</span><span class="sxs-lookup"><span data-stu-id="4c451-103">Writing Custom Exit Modules</span></span>

<span data-ttu-id="4c451-104">Les modules de sortie personnalisés doivent implémenter l’interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , qui est appelée par le moteur serveur.</span><span class="sxs-lookup"><span data-stu-id="4c451-104">Custom exit modules must implement the [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) interface, which is called by the server engine.</span></span> <span data-ttu-id="4c451-105">La méthode [**ICertExit :: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) est appelée par le moteur serveur lorsque le module de sortie est chargé.</span><span class="sxs-lookup"><span data-stu-id="4c451-105">The [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) method is called by the server engine when the exit module is loaded.</span></span> <span data-ttu-id="4c451-106">Elle permet au module de sortie d’effectuer l’initialisation et retourne une valeur qui informe le moteur serveur des types d’événements pour lesquels il souhaite recevoir la notification.</span><span class="sxs-lookup"><span data-stu-id="4c451-106">It allows the exit module to perform initialization and returns a value that informs the server engine of the kinds of events for which it wants notification.</span></span> <span data-ttu-id="4c451-107">La méthode [**ICertExit :: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) doit retourner une chaîne de description lorsque le moteur du serveur le demande.</span><span class="sxs-lookup"><span data-stu-id="4c451-107">The [**ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) method must return a description string when the server engine requests it.</span></span> <span data-ttu-id="4c451-108">La méthode [**ICertExit :: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) est appelée par le moteur du serveur pour informer le module de sortie qu’un événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="4c451-108">The [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) method is called by the server engine to notify the exit module that an event has occurred.</span></span>

<span data-ttu-id="4c451-109">Les modules de sortie peuvent appeler l’interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , qui prend en charge la plupart des méthodes de l’interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , à l’exception des méthodes [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) et [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4c451-109">Exit modules can call the [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) interface, which supports many of the same methods as the [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) interface, with the exception of the [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) and [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) methods.</span></span>

<span data-ttu-id="4c451-110">Pour plus d’informations sur la suppression du module de sortie existant et l’installation d’un nouveau, consultez la rubrique relative à la personnalisation du module de sortie dans l’aide de.</span><span class="sxs-lookup"><span data-stu-id="4c451-110">For information about removing the existing exit module and installing a new one, see the Exit Module Customization topic in Help.</span></span>

 

 




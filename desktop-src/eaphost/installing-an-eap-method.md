---
title: Installation d’une méthode EAP
description: Suivez les instructions ci-dessous pour installer une méthode EAP implémentée par l’utilisateur sur un ordinateur client exécutant EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726285"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="04b48-103">Installation d’une méthode EAP</span><span class="sxs-lookup"><span data-stu-id="04b48-103">Installing an EAP Method</span></span>

<span data-ttu-id="04b48-104">Suivez les instructions ci-dessous pour installer une méthode EAP implémentée par l’utilisateur sur un ordinateur client exécutant EAPHost.</span><span class="sxs-lookup"><span data-stu-id="04b48-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="04b48-105">Implémentez [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) pour votre dll de méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="04b48-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="04b48-106">Ces fonctions ajoutent et suppriment les clés de Registre appropriées pour votre méthode EAP pendant le processus d’installation et de (désinstallation).</span><span class="sxs-lookup"><span data-stu-id="04b48-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="04b48-107">Pour plus d’informations sur les clés de Registre spécifiques associées à l’installation d’une méthode EAP, consultez la rubrique [configuration du Registre pour les méthodes EAP](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="04b48-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="04b48-108">Installez la DLL qui contient l’implémentation de la méthode EAP à l’aide de la commande de console suivante.</span><span class="sxs-lookup"><span data-stu-id="04b48-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="04b48-109"> *&lt; Nom &gt;* de la dllregsvr32.exe</span><span class="sxs-lookup"><span data-stu-id="04b48-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="04b48-110">Pour désinstaller la DLL, utilisez la commande de console suivante :</span><span class="sxs-lookup"><span data-stu-id="04b48-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="04b48-111">**regsvr32.exe** **/u** *&lt; nom &gt;* de la dll</span><span class="sxs-lookup"><span data-stu-id="04b48-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="04b48-112">Redémarrez le service EAPHost.</span><span class="sxs-lookup"><span data-stu-id="04b48-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04b48-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04b48-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b48-114">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="04b48-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 
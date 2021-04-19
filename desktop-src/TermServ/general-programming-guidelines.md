---
title: Instructions de programmation générales
description: Instructions pour le développement d’applications dans un environnement de Services Bureau à distance.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511698"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="3af4a-103">Instructions de programmation générales</span><span class="sxs-lookup"><span data-stu-id="3af4a-103">General programming guidelines</span></span>

<span data-ttu-id="3af4a-104">Les sections suivantes fournissent des recommandations générales pour le développement d’applications dans un environnement de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3af4a-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3af4a-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3af4a-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3af4a-106">Couche de compatibilité des applications</span><span class="sxs-lookup"><span data-stu-id="3af4a-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="3af4a-107">Pour exécuter des applications héritées dans un environnement Services Bureau à distance, vous pouvez utiliser la couche de compatibilité des applications Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="3af4a-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="3af4a-108">Instructions pour les applications client/serveur</span><span class="sxs-lookup"><span data-stu-id="3af4a-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="3af4a-109">Les applications client/serveur ne doivent pas supposer qu’une seule connexion d’ordinateur équivaut à une seule session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3af4a-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="3af4a-110">Surveillance des connexions et des déconnexions de session</span><span class="sxs-lookup"><span data-stu-id="3af4a-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="3af4a-111">Pour inscrire une application avec Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé.</span><span class="sxs-lookup"><span data-stu-id="3af4a-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="3af4a-112">Instructions relatives au matériel périphérique</span><span class="sxs-lookup"><span data-stu-id="3af4a-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="3af4a-113">Si leur périphérique matériel n’est pas conçu pour fonctionner sur une session à distance, les fournisseurs doivent s’assurer que le logiciel du pilote de périphérique force la désactivation de la redirection de l’appareil à l’aide d’une stratégie système ou d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3af4a-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="3af4a-114">Liaison au moment de l’exécution à Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="3af4a-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="3af4a-115">Votre application peut utiliser l’API Services Bureau à distance pour établir une liaison dynamique avec l' Wtsapi32.dll au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3af4a-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="3af4a-116">Pour ce faire, votre application doit appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="3af4a-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 
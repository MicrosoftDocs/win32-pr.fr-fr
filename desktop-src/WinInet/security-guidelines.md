---
title: Indications de sécurité
description: Il est important de tenir l’utilisateur informé des problèmes de sécurité possibles.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102109"
---
# <a name="security-guideline"></a><span data-ttu-id="42279-103">Indications de sécurité</span><span class="sxs-lookup"><span data-stu-id="42279-103">Security Guideline</span></span>

<span data-ttu-id="42279-104">Il est important de tenir l’utilisateur informé des problèmes de sécurité possibles.</span><span class="sxs-lookup"><span data-stu-id="42279-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="42279-105">Notifier l’utilisateur de Security-Related événements</span><span class="sxs-lookup"><span data-stu-id="42279-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="42279-106">Informez toujours l’utilisateur de toute modification de la sécurité, qu’il s’agisse d’une erreur liée à la sécurité, telle qu’un échec de certificat ou d’une modification de la sécurité du protocole sous-jacent, telle que la modification d’un site HTTPs en un site HTTP.</span><span class="sxs-lookup"><span data-stu-id="42279-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="42279-107">Notifier l’utilisateur des erreurs de Security-Related</span><span class="sxs-lookup"><span data-stu-id="42279-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="42279-108">Lorsque votre application reçoit un message d’erreur qui peut indiquer un problème de sécurité, la fonction **InternetErrorDlg** fournit une interface standard et familière pour la notification de l’utilisateur dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="42279-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="42279-109">Parmi les erreurs qui se trouvent dans cette catégorie, citons les suivantes :</span><span class="sxs-lookup"><span data-stu-id="42279-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="42279-110">**ERREUR \_ Internet \_ http \_ à \_ https \_ sur le \_ ReDim**</span><span class="sxs-lookup"><span data-stu-id="42279-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="42279-111">**ERREUR \_ Internet \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="42279-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="42279-112">**ERREUR \_ Internet \_ poster \_ \_ non \_ sécurisée**</span><span class="sxs-lookup"><span data-stu-id="42279-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="42279-113">**\_Erreurs de \_ certificat Internet s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42279-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="42279-114">**ERREUR \_ de \_ certificat CN de l’Internet s \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="42279-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="42279-115">**ERREUR \_ Internet \_ sec \_ date du certificat \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="42279-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="42279-116">Un échec de notification à l’utilisateur des erreurs telles que celles-ci peut exposer l’utilisateur à divers types de violations de sécurité, y compris les attaques par usurpation d’identité ou la divulgation d’informations involontaires.</span><span class="sxs-lookup"><span data-stu-id="42279-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="42279-117">Notifier l’utilisateur lorsque la sécurité de la connexion change</span><span class="sxs-lookup"><span data-stu-id="42279-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="42279-118">Informez toujours l’utilisateur lorsque la sécurité de la connexion change, par exemple du protocole HTTPs à HTTP.</span><span class="sxs-lookup"><span data-stu-id="42279-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="42279-119">Dans le cas contraire, sauf si l’utilisateur a explicitement choisi de ne pas être informé de ces modifications, vous dissimulez les risques de divulgation involontaire des informations.</span><span class="sxs-lookup"><span data-stu-id="42279-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="42279-120">Parmi les fonctions qui signalent une telle modification dans la sécurité de connexion, citons la fonction de rappel **InternetStatusCallback** et la fonction **InternetConfirmZoneCrossing** .</span><span class="sxs-lookup"><span data-stu-id="42279-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="42279-121">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="42279-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="42279-122">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="42279-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="42279-123">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="42279-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 